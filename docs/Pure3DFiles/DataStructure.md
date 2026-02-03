---
title: "Data Structure"
description: "Information on the data structure of Pure3D Files."
authors: [ 2, 6310 ]
---

Pure3D files are made up of a hierarchy of chunks containing a wide variety of data.

This page outlines what primitives and data types you will encounter in Pure3D files and the general structure of these files.

# Primitives
| Primitive | Data Size              |
|-----------|------------------------|
| int8      | 1 byte                 |
| int16     | 2 bytes                |
| int32     | 4 bytes                |
| uint8     | 1 byte                 |
| uint16    | 2 bytes                |
| uint32    | 4 bytes                |
| float     | 4 bytes                |
| char      | 1 byte                 |
| string    | 1 byte + string length |
| bool      | 4 bytes                |

# Data Types
| Data Type          | Data Size | Structure                                                                                                                                                                              |
|--------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vector2            | 8 bytes   | float X, float Y                                                                                                                                                                       |
| Vector3            | 12 bytes  | float X, float Y, float Z                                                                                                                                                              |
| Quaternion         | 16 bytes  | float W, float X, float Y, float Z                                                                                                                                                     |
| Matrix4x4          | 64 bytes  | float M11, float M12, float M13, float M14,<br>float M21, float M22, float M23, float M24,<br>float M31, float M32, float M33, float M34<br>float M41, float M42, float M43, float M44 |
| SymmetricMatrix3x3 | 24 bytes  | float XX, float XY, float XZ,<br>float YY, float YZ,<br>float ZZ                                                                                                                       |
| Colour             | 4 bytes   | uint8 R, uint8 G, uint8 B, uint8 A                                                                                                                                                     |

# File Signatures
| Hex Signature | Text Signature | Description              |
|---------------|----------------|--------------------------|
| 50 33 44 FF   | P3Dÿ           | Little Endian (Standard) |
| FF 44 33 50   | ÿD3P           | Big Endian               |
| 50 33 44 5A   | P3DZ           | Little Endian Compressed |
| 5A 44 33 50   | ZD3P           | Big Endian Compressed    |

# File Structure
A Pure3D file is at least 12 bytes containing the following data:

| Property   | Data Type | Description                                                       |
|------------|-----------|-------------------------------------------------------------------|
| Signature  | int32     | The file's signature.                                             |
| HeaderSize | int32     | The size of the file's header. Always 12.                         |
| Size       | int32     | The entire size of the file, including the header and all chunks. |

The file signature indicates if the file is compressed or not, as well as the endianness of all data after it, including the file's own **HeaderSize** and **Size**.

If the file has a compressed signature, you must first decompress it to read the data. See [LZR Compression](#lzr-compression) below for more details.

If the file was not compressed to begin with or has been decompressed, you can then start reading chunks following the header.

There can be 0 or more chunks following the header and each is structured similarly to the file itself:

| Property   | Data Type | Description                                                       |
|------------|-----------|-------------------------------------------------------------------|
| Type       | int32     | An identifier indicating what type of chunk this is.              |
| HeaderSize | int32     | The size of the chunk's header and data.                          |
| Size       | int32     | The size of the chunk's header and data, as well as its children. |

Child chunks are stored after the chunk's header.

# LZR Compression
TODO