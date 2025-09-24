# Minecraft-PE-Native-Function-Mapping-Table
Minecraft: PE 原生函数与部分字段映射表

此表自用  
_This table is for my person use_

所有地址和偏移由 TheChuan1503 分析  
_All addresses and offsets are analyzed by TheChuan1503_

使用和分享此表必须遵守 [CC BY-NC-4.0](LICENSE.zh) 许可证  
_Use and share this table under the [CC BY-NC-4.0](LICENSE) license_

# Content
- [Minecraft-PE-Native-Function-Mapping-Table](#minecraft-pe-native-function-mapping-table)
- [Content](#content)
- [Table](#table)
  - [1.16.201.01\_arm64-v8a](#11620101_arm64-v8a)
    - [AABB](#aabb)
    - [Abilities](#abilities)
    - [Actor](#actor)
    - [Camera](#camera)
    - [ClientInstance](#clientinstance)
    - [GameMode](#gamemode)
    - [GuiData](#guidata)
    - [Level](#level)
    - [LevelRendererPlayer](#levelrendererplayer)
    - [LocalPlayer](#localplayer)
    - [Minecraft](#minecraft)
    - [MinecraftGame](#minecraftgame)
    - [Mob](#mob)
    - [MobEffectInstance](#mobeffectinstance)
    - [Player](#player)
    - [PlayerRewindContext](#playerrewindcontext)
    - [PlayerSnapshot](#playersnapshot)
    - [Timer](#timer)
  - [1.16.210.05\_arm64-v8a](#11621005_arm64-v8a)
    - [Abilities](#abilities-1)
    - [Actor](#actor-1)
    - [ActorEventCoordinator](#actoreventcoordinator)
    - [BossComponent](#bosscomponent)
    - [BlockPosTrackerComponent](#blockpostrackercomponent)
    - [ClientInstance](#clientinstance-1)
    - [ClientNetworkHandler](#clientnetworkhandler)
    - [EntityContextBase](#entitycontextbase)
    - [FunctionManager](#functionmanager)
    - [GameMode](#gamemode-1)
    - [GuiData](#guidata-1)
    - [ItemUseInventoryTransaction](#itemuseinventorytransaction)
    - [Level](#level-1)
    - [LocalPlayer](#localplayer-1)
    - [MobEffectInstance](#mobeffectinstance-1)
    - [MobEvents](#mobevents)
    - [NetworkIdentifier](#networkidentifier)
    - [OwnerStorageEntity](#ownerstorageentity)
    - [Player](#player-1)
    - [ServerLevel](#serverlevel)
    - [ServerNetworkHandler](#servernetworkhandler)
    - [ServerPlayer](#serverplayer)
    - [SurvivalMode](#survivalmode)
    - [UpdatePlayerGameTypePacket](#updateplayergametypepacket)

# Table
## 1.16.201.01_arm64-v8a
- jint **JNI_OnLoad** (JavaVM* vm, void* reserved)  
  `0x41A6BDC`

### AABB
- AABB* **AABB::expand** (Vec3 const& direction)  
  `0x5F97FE8`

### Abilities
- _void **Abilities::Abilities** (Abilities* this)_  
  `0x642157C`
- bool **Abilities::getBool** (int index)  
  `0x6423020`

### Actor
- void **Actor::addEffect** (const MobEffectInstance* mobEffectInstance)  
  `0x6688354`
- bool **Actor::canFly** ()  
  `0x6676940`
- bool **Actor::canPowerJump** ()  
  `0x6676A90`
- float **Actor::distanceTo** (Actor* target)  
  `0x66750AC`
- std::vector\<DistanceSortedActor\> **Actor::fetchNearbyActorsSorted** (const Vec3& position, ActorType type)  
  `0x668D148`
- AABB* **Actor::getAABBShapeComponent** ()  
  `0x666BB94`
- float **Actor::getCameraDistance** () const  
  `0x66882C4`
- Vec3* **Actor::getPos** ()  
  `0x666EBCC`
- bool **Actor::getStatusFlag** (ActorFlags flag) const  
  `0x666B670`
- bool **Actor::isAlive** ()  
  `0x66785FC`
- bool **Actor::isLocalPlayer** ()  
  `0x66785D4`
- void **Actor::setCanFly** (bool canFly)  
  `0x6676968`
- void **Actor::setPos** (const Vec3* pos)  
  `0x666E938`

### Camera
- Vec3* **Camera::getPosition** ()  
  `0x55F0C14`

### ClientInstance
- GuiData* **ClientInstance::getGuiData** ()  
  `0x55198C8`
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x5510B58`
- bool **ClientInstance::isInGame** ()  
  `0x55177A4`
- void **ClientInstance::requestLeaveGame** (bool immediateExit, bool suppressConfirmation)  
  `0x550C414`
- void **ClientInstance::tick** ()  
  `0x550E108`
- bool **ClientInstance::update** (bool forceUpdate)  
  `0x550E1F0`

### GameMode
- bool **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0x634D43C`
- float **GameMode::getMaxPickRange** ()  
  `0x634F960`
- bool **GameMode::startDestroyBlock** (const BlockPos& pos, unsigned char face, bool& outResult)  
  `0x634CFCC`

### GuiData
- void **GuiData::displayClientMessage** (std::string const& message)  
  `0x541E76C`
- void **GuiData::setActionBarMessage** (std::string const& message)  
  `0x5420B20`
- void **GuiData::setGuiScale** (float scale)  
  `0x5420718`
- void **GuiData::setSubtitle** (std::string const& message)  
  `0x5420A5C`
- void **GuiData::setTitle** (std::string const& message)  
  `0x54209D4`
- void **GuiData::showTipMessage** (std::string const& message)  
  `0x541F844`

### Level
- bool **Level::destroyBlock** (BlockSource& source, const BlockPos& pos, bool dropResources)  
  `0x61BD3B8`
- std::vector\<Actor\*> **Level::getRuntimeActorList** () const  
  `0x61BDAA4`
- void **Level::tick** ()  
  `0x61B4C50`

### LevelRendererPlayer
- float **LevelRendererPlayer::getFov** (float baseFov, bool useSmoothTransition)  
  `0x5999834`

### LocalPlayer
- void **LocalPlayer::addLevels** (int levels)  
  `0x5BA7658`
- float **LocalPlayer::getPickRange** ()  
  `0x5BA7B5C`
- bool **LocalPlayer::isFlying** ()  
  `0x5BA27E0`
- void **LocalPlayer::jumpFromGround** ()  
  `0x5BA7C98`
- void **LocalPlayer::setPlayerGameType** (GameType type)  
  `0x5BA5C5C`
- void **LocalPlayer::setPlayerGameTypeWithoutServerNotification** (GameType type)  
  `0x5BA5D14`
- void **LocalPlayer::setPos** (Vec3 const& pos)  
  `0x5BA2DFC`

### Minecraft
- Timer* **Minecraft::getTimer** ()  
  `0x6A24930`
- void **Minecraft::setGameModeReal** (GameType type)  
  `0x6A23344`
- void **Minecraft::update** ()  
  `0x6A23390`

### MinecraftGame
- void* **MinecraftGame::getInput** ()  
  `0x5572D5C`
- void **MinecraftGame::tickInput** ()  
  `0x5561998`

### Mob
- bool **Mob::isSprinting** ()  
  `0x6643C84`

### MobEffectInstance
- _void **MobEffectInstance::MobEffectInstance** (MobEffectInstance* this, unsigned int effectId, int durationTicks, int level, bool b1, bool effectVisible, bool b2)_  
  `0x63B73F0`

### Player
- bool **Player::attack** (Actor* target)  
  `0x6438CE0`
- float **Player::getAttackDamage** ()  
  `0x643E2C0`
- float **Player::getCameraOffset** ()  
  `0x6437E10`
- GameType **Player::getPlayerGameType** ()  
  `0x643F78C`
- float **Player::getSpeed** ()  
  `0x642C3B4`

### PlayerRewindContext
- bool **PlayerRewindContext::isOnGround** ()  
  `0x5C4C2E8`
- bool **PlayerRewindContext::isSprinting** ()  
  `0x5C4D128`

### PlayerSnapshot
- _void **PlayerSnapshot::PlayerSnapshot** (PlayerSnapshot* this)_  
  `0x5650584`

### Timer
- int **mTicksPerSecond**  
  `+0x48`
  
   ---
- _void **Timer::Timer** (Timer* this)_  
  `0x421A85C`
- float **Timer::getTimeScale** ()  
  `0x421A970`
- void **Timer::setTimeScale** (float scale)  
  `0x421A980`

## 1.16.210.05_arm64-v8a
_此表未经完全验证_

- jint **JNI_OnLoad** (JavaVM* vm, void* reserved)  
  `0x1DA1A20`

### Abilities
- bool **Abilities::getBool** (AbilitiesIndex index)  
  `0x281D644`

### Actor
- bool **mIsAlive**  
  `+0x3A9`

  ---
- void **Actor::addEffect** (const MobEffectInstance* mobEffectInstance)  
  `0x24ED9C4`
- float **Actor::distanceTo** (Actor const&)  
  `0x24DA18C`
- Vec3* **Actor::getPos** ()  
  `0x24D15D4`
- char* **Actor::getUniqueID** ()  
  `0x24CEA00`
- bool **Actor::isAlive** ()  
  `0x24DD7F4`
- void **Actor::remove** ()  
  `0x24D48D0`
- void **Actor::setPos** (const Vec3* pos)  
  `0x24D3CF0`

### ActorEventCoordinator
- void **ActorEventCoordinator::sendActorRemoved** (Actor*)  
  `0x21659C4`

### BossComponent
- void **BossComponent::unRegisterPlayer** (Actor*, Player*)  
  `0x1BFE344`

### BlockPosTrackerComponent
- void **BlockPosTrackerComponent::onRemove** (Actor*)  
  `0x5A1B3D4`

### ClientInstance
- GuiData* **mGuiData**  
  `+0x4b0` ?
- LocalPlayer* **mLocalPlayer**  
  `+0x118`

  ---
- void **ClientInstance::_updateScreenSizeVariables** (Vec2 const&, float, float, float)  
  `0x34B64E4`
- DateManager* **ClientInstance::getDateManager** ()  
  `0x34BBF58`
- GuiData* **ClientInstance::getGuiData** ()  
  `0x34BBF40` ?
- LocalPlayer* **ClientInstance::getLocalPlayer** ()  
  `0x34B0FE0`
- bool **ClientInstance::isInGame** ()  
  `0x34B99D4`
- void **ClientInstance::requestLeaveGame** (bool immediateExit, bool suppressConfirmation)  
  `0x34B99C4`
- void **ClientInstance::startExternalNetworkWorld** (Social::GameConnectionInfo, std::string const&, bool)  
  `0x34AC780`
- void **ClientInstance::update** (bool forceUpdate)  
  `0x34AE5BC`

### ClientNetworkHandler
- void **ClientNetworkHandler::handle** (const NetworkIdentifier *, const SetTitlePacket *)  
  `0x37E3A48`
- void **ClientNetworkHandler::handle** (const NetworkIdentifier *, const TextPacket *)  
  `0x37DB9FC` ?

### EntityContextBase
- **EntityContextBase::_enttRegistry** ()  
  `0x1D2DB18`

### FunctionManager
- void **FunctionManager::tick** ()  
  `0x1DFCB30`

### GameMode
- bool **GameMode::destroyBlock** (BlockPos const& pos, unsigned char face)  
  `0x20EB8C0`
- float **GameMode::getMaxPickRange** ()  
  `0x20EDC78`

### GuiData
- void **GuiData::displayClientMessage** (std::string const& message)  
  `0x3310FB4`
- void **GuiData::setActionBarMessage** (std::string const& message)  
  `0x3313E5C`
- void **GuiData::setGuiScale** (float scale)  
  `0x3313A58` ?
- void **GuiData::setSubtitle** (std::string const& message)  
  `0x3313D98`
- void **GuiData::setTitle** (std::string const& message)  
  `0x3313D10`
- void **GuiData::showTipMessage** (std::string const& message)  
  `0x3312AB0`

### ItemUseInventoryTransaction
- void **ItemUseInventoryTransaction::handle** (Player*, bool)  
  `0x20D329C`

### Level
- void **Level::tick** ()
  `0x2E9DCE0`

### LocalPlayer
- void **LocalPlayer::displayClientMessage** (std::string const& message)  
  `0x36FBEAC`
- void **LocalPlayer::startRiding** (Actor *)  
  `0x37000EC`
- void **LocalPlayer::stopSpinAttack** ()  
  `0x36FBE2C`

### MobEffectInstance
- bool **MobEffectInstance::operator!=** (MobEffectInstance const&)  
  `0x2164324`

### MobEvents
- void **MobEvents::tick** ()  
  `0x2EAD348`

### NetworkIdentifier
- bool **NetworkIdentifier::equalsTypeData** (NetworkIdentifier const&)  
  `0x17F2D4C`

### OwnerStorageEntity
- **OwnerStorageEntity::_getStackRef** ()  
  `0x17B3DD0`
- **OwnerStorageEntity::_hasValue** ()  
  `0x17B3C14`

### Player
- GameType **Player::getPlayerGameType** ()  
  `0x283AEAC`
- int **Player::getClientSubId** ()  
  `0x28266EC`
- void **Player::setPlayerGameType** (GameType type)  
  `0x283A66C`

### ServerLevel
- void **ServerLevel::tick** ()
  `0x1E11794`

### ServerNetworkHandler
- void **ServerNetworkHandler::handle** (Level **this, const NetworkIdentifier* networkIdentifier, const InteractPacket* packet)  
  `0x1921758`

### ServerPlayer
- bool **ServerPlayer::isValidTarget** (Actor*)  
  `0x1E16384`
- void **ServerPlayer::sendMobEffectPackets** ()  
  `0x1E1CDA0` 
- void **ServerPlayer::setPlayerGameType** (Actor* actor, GameType type)  
  `0x1E1CD08`

### SurvivalMode
- void **SurvivalMode::destroyBlock** (const BlockPos *, unsigned __int8)  
  `0x20EE4BC`

### UpdatePlayerGameTypePacket
- _void **UpdatePlayerGameTypePacket::UpdatePlayerGameTypePacket** (UpdatePlayerGameTypePacket* this, GameType gameType, ActorUniqueID const& actorUniqueId)_  
  `0x1F00390`