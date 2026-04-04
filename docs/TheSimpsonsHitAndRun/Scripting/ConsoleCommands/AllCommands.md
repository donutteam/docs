---
title: "All Console Script Commands"
title_hierarchy: "All Commands"
description: "A listing of all console script commands."
authors: [ 2 ]
---

This page lists all Console Script commands that exist in the base game.

Console scripts use one of two file extensions: `.con` (for configuring a car's stats) and `.mfk` (for configuring rewards, levels and missions).

# CON Commands
These commands are used in `.con` files to configure a car's stats and other aspects of the car.
* [[SetAllowSeatSlide.md]]
* SetBrakeScale
* SetBurnoutRange
* [[SetCharacterScale.md]]
* [[SetCharactersVisible.md]]
* SetCMOffsetX
* SetCMOffsetY
* SetCMOffsetZ
* SetDamperC
* SetDonutTorque
* [[SetDriver.md]]
* SetEBrakeEffect
* SetGamblingOdds
* SetGasScale
* SetGasScaleSpeedThreshold
* [[SetHasDoors.md]]
* SetHighRoof
* SetHighSpeedGasScale
* SetHighSpeedSteeringDrop
* SetHitPoints
* SetMass
* SetMaxSpeedBurstTime
* SetMaxWheelTurnAngle
* SetNormalSteering
* [[SetIrisTransition.md]]
* SetShadowAdjustments
* SetShininess
* SetSlipEffectNoEBrake
* SetSlipGasScale
* SetSlipSteering
* SetSlipSteeringNoEBrake
* SetSpringK
* SetSuspensionLimit
* SetSuspensionYOffset
* SetTireGrip
* SetTopSpeedKmh
* [[SetWeebleOffset.md]]
* [[SetWheelieOffsetY.md]]
* [[SetWheelieOffsetZ.md]]
* [[SetWheelieRange.md]]

# MFK Commands
These commands are used throughout various types of `.mfk` scripts.

The commands in this section are categorized by what "scope" they are valid within, such as within a mission or an objective.

Additionally, commands where all of Radical's usages are **Commented** out or that are fully **Unused** in Radical's scripts will be marked as such.

## General
These are general commands that can be used in multiple scopes.
* [[InitLevelPlayerVehicle.md]]
* [[LoadP3DFile.md]]
* SetPresentationBitmap
* **Collectibles**
	* SetRespawnRate (Unused)
* **Dialog**
	* [[AddAmbientPcAnimation.md]]
	* [[AddAmbientNpcAnimation.md]]
	* SetCamBestSide
	* SetConversationCam
* **Triggers**
	* ActivateTrigger (Unused)
	* DeactivateTrigger (Unused)

## Reward Initialisation
These are commands used in the game's rewards script (`rewards.mfk`) to add cars to the phonebooth and skins to skin shops.
* [[BindReward.md]]
* [[SetCarAttributes.md]]
* SetTotalGags
* SetTotalWasps (Unused)

## Level Load
These are commands used in a level's load script (`level.mfk`).
* AddBonusMission
* AddMission
* AddTeleportDest
* SetStatepropShadow
* [[SuppressDriver.md]]
* **Gag Bindings**
	* AddGagBinding
	* ClearGagBindings
* **Gags**
	* [[GagBegin.md]]
	* GagCheckCollCards
	* GagCheckMovie
	* [[GagEnd.md]]
	* GagPlayFMV
	* GagSetAnimCollision
	* GagSetCameraShake
	* GagSetCoins
	* GagSetCycle
	* [[GagSetInterior.md]]
	* GagSetIntro
	* GagSetLoadDistances (Unused)
	* GagSetOutro
	* [[GagSetPersist.md]]
	* [[GagSetPosition.md]]
	* GagSetRandom
	* GagSetSound
	* GagSetSoundLoadDistances
	* [[GagSetSparkle.md]]
	* GagSetTrigger
	* GagSetWeight (Unused)

## Level Initialisation
These are commands used in a level's initialisation script (`leveli.mfk`).
* AddCharacter
* EnableTutorialMode
* SetCoinDrawable
* SetParticleTexture
* **Actors**
	* AddBehaviour
	* AddFlyingActor (Unused)
	* AddFlyingActorByLocator
	* AddShield
	* [[AddSpawnPoint.md]] (Commented)
	* [[AddSpawnPointByLocatorScript.md]]
	* PreallocateActors
	* SetActorRotationSpeed
	* SetCollisionAttributes (Unused)
	* SetProjectileStats
* **Ambient NPCs**
	* AddAmbientCharacter
* **Bonus Mission NPCs**
	* AddBonusMissionNPCWaypoint
	* [[AddNPCCharacterBonusMission.md]]
	* [[ClearAmbientAnimations.md]]
	* SetBonusMissionDialoguePos
* **Car Shop NPCs**
	* AddPurchaseCarNPCWaypoint
	* AddPurchaseCarReward
* **Chase Manager**
	* [[CreateChaseManager.md]]
	* [[SetHitAndRunDecay.md]]
	* [[SetHitAndRunDecayInterior.md]] (Unused)
	* [[SetNumChaseCars.md]]
* **Ped Groups**
	* [[AddPed.md]]
	* [[CreatePedGroup.md]]
	* [[ClosePedGroup.md]]
* **Traffic Groups**
	* [[AddTrafficModel.md]]
	* [[CreateTrafficGroup.md]]
	* [[CloseTrafficGroup.md]]

## Mission Load
These are commands used in a mission's load script.
* LoadDisposableCar

## Mission Initialisation
These are commands used in a mission's initialisation script.
* AddCollectibleStateProp
* [[CloseMission.md]]
* PlacePlayerCar
* [[SelectMission.md]]
* SetAnimatedCameraName
* SetAnimCamMulticontName
* [[SetDynaLoadData.md]]
* [[SetForcedCar.md]]
* [[SetInitialWalk.md]]
* [[SetMissionResetPlayerInCar.md]]
* [[SetMissionResetPlayerOutCar.md]]
* SetMissionStartCameraName
* SetMissionStartMulticontName
* SetNumValidFailureHints
* ShowHUD
* [[StreetRacePropsLoad.md]]
* [[StreetRacePropsUnload.md]]
* [[UsePedGroup.md]]
* **Stages**
	* [[ActivateVehicle.md]]
	* AddSafeZone
	* [[AddStage.md]]
	* AddStageCharacter
	* AddStageMusicChange
	* [[AddStageTime.md]]
	* [[AddStageVehicle.md]]
	* AddStageWaypoint
	* AllowMissionAbort
	* AmbientAnimationRandomize
	* ClearTrafficForStage
	* [[CloseStage.md]]
	* DisableHitAndRun
	* GoToPsScreenWhenDone
	* MoveStageVehicle (Unused)
	* msPlacePlayerCarAtLocatorName (Unused)
	* PlacePlayerAtLocatorName (Unused)
	* PutMFPlayerInCar
	* NoTrafficForStage
	* [[RESET_TO_HERE.md]]
	* SetCharacterToHide
	* SetCompletionDialog
	* SetConversationCamName
	* SetConversationCamPcName (Commented)
	* SetConversationCamNpcName (Commented)
	* [[SetFadeOut.md]]
	* SetGameOver
	* [[SetHUDIcon.md]]
	* [[SetIrisWipe.md]]
	* SetLevelOver
	* [[SetMaxTraffic.md]]
	* [[SetMusicState.md]]
	* SetRaceEnteryFee
	* SetStageAIEvadeCatchupParams
	* SetStageAIRaceCatchupParams
	* SetStageAITargetCatchupParams
	* SetStageCamera (Unused)
	* [[SetStageMessageIndex.md]]
	* SetStageMusicAlwaysOn
	* [[SetStageTime.md]]
	* SetSwapDefaultCarLocator
	* SetSwapForcedCarLocator
	* SetSwapPlayerLocator
	* SetVehicleAIParams
	* ShowStageComplete
	* [[StageStartMusicEvent.md]]
	* StayInBlack
	* SwapInDefaultCar
	* [[UseElapsedTime.md]]
	* **Countdowns**
		* AddToCountdownSequence
		* StartCountdown
	* **Objectives**
		* AddCollectible
		* [[AddDriver.md]]
		* [[AddNPC.md]]
		* [[AddObjective.md]]
		* [[AddObjectiveNPCWaypoint.md]]
		* AllowRockOut
		* AllowUserDump (Unused)
		* [[BindCollectibleTo.md]]
		* [[CloseObjective.md]]
		* MustActionTrigger
		* RemoveDriver
		* RemoveNPC
		* SetCoinFee
		* SetCollectibleEffect
		* SetDestination
		* SetDialogueInfo
		* SetDialoguePositions
		* [[SetDurationTime.md]]
		* SetFMVInfo
		* SetObjDistance
		* SetObjTargetBoss
		* SetObjTargetVehicle
		* SetParTime
		* SetPickupTarget
		* SetRaceLaps
		* [[SetTalkToTarget.md]]
		* TurnGotoDialogOff
	* **Conditions**
		* [[AddCondition.md]]
		* [[CloseCondition.md]]
		* SetConditionPosition
		* SetCondMinHealth
		* SetCondTargetVehicle
		* SetCondTime
		* SetFollowDistances

# Miscellaneous Commands
These are miscellaneous commands that do *something* but how they were meant to be used is unclear.
* [[KillAllChaseAI.md]]

# Dummy Commands
These commands either do literally or effectively nothing in the release game.
* AddGlobalProp (Unused)
* AddVehicleSelectInfo
* ClearVehicleSelectInfo (Unused)
* CreateAnimPhysObject (Unused)
* LinkActionToObject (Unused)
* LinkActionToObjectJoint (Unused)
* SetCarStartCamera (Unused)
* SetHitNRun
* SetMissionNameIndex (Unused)
* SetPostLevelFMV

# Uncategorized Commands
These commands have not yet been categorized on this page.
* AddBonusObjective (Unused)
* AttachStatePropCollectible (Commented)
* CharacterIsChild (Unused)
* CreateActionEventTrigger (Unused)
* EnableHitAndRun (Unused)
* ResetCharacter (Unused)
* ResetHitAndRun (Unused)
* SetBonusMissionStart (Unused)
* SetCharacterPosition (Unused)
* SetChaseSpawnRate (Commented)
* SetConversationCamDistance (Unused)
* SetDemoLoopTime
* SetHitAndRunMeter (Commented)
* SetPlayerCarName (Unused)
* SetVehicleToLoad (Unused)