Title: Config-Files

# Config-Files

AntiCooldown is fully adjustable by the user. Almost every detail can be changed through the config. If anything is unclear, our (support)[https://yourgamespace.com/support/] is always available!

## Config.yml

```yaml
# All messages of AntiCooldown
Messages:
  # Prefix for chat messages
  Prefix: '§7[§3AntiCooldown§7] '
  # Prefix for actionbar messages
  ActionBarPrefix: §3AntiCooldown§7 »

  # Messages related to a world switch
  SwitchWorld:
    # Message when the world is deactivated but the player has bypass permissions
    # Bypass-Permission: anticooldown.bypass
    Bypassed: §ePvP Cooldown is §c§lnot disabled §ein this world, but you have §2Bypass-Permissions§a!
      §aCooldown is disable for you.
    # Message when the cooldown is deactivated in the world
    Enabled: §ePvP Cooldown is §a§ldisabled §ein this world!
    # Message when the cooldown is activated in the world
    Disabled: §ePvP Cooldown is §c§lnot disabled §ein this world!

  # Messages related to player login
  Login:
    # Message when the world is deactivated but the player has bypass permissions
    # Bypass-Permission: anticooldown.bypass
    Bypassed: §aHey, welcome to the server! §ePvP Cooldown is §c§lnot disabled §ein
      this world, but you have §2Bypass-Permissions§a! §aCooldown is disable for you.
    # # Message when the cooldown is deactivated in the world
    Enabled: §aHey, welcome to the server! §ePvP Cooldown is §a§ldisabled §ein this
      world!
    # Message when the cooldown is activated in the world
    Disabled: §aHey, welcome to the server! §ePvP Cooldown is §c§lnot disabled §ein
      this world!

  # Messages related to the CustomItemDamage module
  CustomItemDamage:
    # Message that is displayed as an ActionBar and informs the player about the custom damage
    ActionBarMessage: '%actionbar_prefix% §aCustom-Damage applied: §7%finaldamage%§c❤
      §7Damage'

  # Messages related to the ItemRestriction module
  ItemRestriction:
    # Message that is displayed as an ActionBar and informs the player about the custom damage
    ActionBarMessage:
      # Message as ActionBar, which is displayed when the item is deactivated
      Enabled: '%actionbar_prefix% §aItem is no longer restricted! PvP Cooldown is
        §a§ldisabled §aagain'
      # Message as ActionBar, which is displayed when the item is activated
      Disabled: '%actionbar_prefix% §cItem is restricted! PvP Cooldown is temporarily
        §c§lactivated'

  # Messages related to ingame commands and/or settings
  Setting:
    # Message when a world will be disabled
    AddDisabledWorld: §aOK! In the world §e%world% §athe cooldown is now activated.
    # Message when a world will be enabled
    RemoveDisabledWorld: §aOK! In the world §e%world% §athe cooldown is now deactivated.

  # Messages related to errors
  Error:
    # Message when a world is already disabled
    WorldAlreadyDisabled: §cThis world is already §c§ldeactivated§c!
    # Message when a world is already enabled
    WorldAlreadyEnabled: §cThis world is already §a§lactivated§c!
    # Message when the player is not online
    # Mainly used for commands
    PlayerNotOnline: §cThe player is not online!
    # Message if a player try to use commands and has no permissions
    NoPerms: §cNo permissions!

# Content of placerholders
Placeholder:
  # Placeholder related to world cooldown
  # Placeholder: anticooldown_worldcooldown
  World:
    # The content which is returned with the above placeholder,
    # if the cooldown is enabled in the world.
    CooldownEnabled: Enabled
    # The content which is returned with the above placeholder,
    # if the cooldown is disabled in the world.
    CooldownDisabled: Disabled
  # Placeholder related to players cooldown
  # Placeholder: anticooldown_playercooldown
  Player:
    # The content which is returned with the above placeholder,
    # if the cooldown is enabled for the player.
    CooldownEnabled: Enabled
    # The content which is returned with the above placeholder,
    # if the cooldown is disabled for the player.
    CooldownDisabled: Disabled

# Setting options of AntiCooldown
Settings:
  # Settings related to permissions
  Permissions:
    # Determines whether permissions are to be used
    # Available options: true, false
    UsePermissions: false
    # Sets whether to use the bypass permissions.
    # Note: Bypass permissions are not dependent on the UsePermissions option
    # Available options: true, false
    UseBypassPermission: false
  Messages:
    # Determines whether the player should be sent a message
    # about the current cooldown status when logging in.
    # Available options: true, false
    UseLoginMessage: true
    # Determines whether the player should be sent a message
    # about the current cooldown status when switching worlds.
    # Available options: true, false
    UseSwitchWorldMessage: true

  # All values which are used by AntiCooldown
  Values:
    # Sets the BaseAttackSpeed which is used for the cool down deactivation
    # 16 is the minimum value for the cool-down to be deactivated
    # Recommended: 100 - This makes the cooldown indicator invisible
    AttackSpeed: 100
    # Worlds in which AntiCooldown is not active
    DisabledWorlds:
    - YourWorldName
    # Item that the player can hold in their hand and temporarily reactivate the player's cooldown.
    # This item list can also be used as a whitelist, so that the cooldown is only deactivated if
    # the player is holding one of the items entered here. Requires the activation of UseAsWhitelist.
    RestrictedItems:
    - DIAMOND_AXE
    - GOLDEN_AXE
    - IRON_AXE
    - STONE_AXE
    - NETHERITE_AXE
    - WOODEN_AXE
    # The base damage value of an item can be overwritten here
    # SYNTAX: ITEM:DAMAGE
    # NOTE: The damage is of the data type "Double", it is therefore necessary to specify "D" after the value,
    # as in the already existing entries!
    # Material-List of the latest Spigot version:
    # https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html
    CustomItemDamage:
    - WOOD_AXE:3.0D
    - WOODEN_AXE:3.0D
    - GOLD_AXE:3.0D
    - GOLDEN_AXE:3.0D
    - STONE_AXE:4.0D
    - IRON_AXE:5.0D
    - DIAMOND_AXE:6.0D
    - WOOD_PICKAXE:2.0D
    - WOODEN_PICKAXE:2.0D
    - GOLD_PICKAXE:2.0D
    - GOLDEN_PICKAXE:2.0D
    - STONE_PICKAXE:3.0D
    - IRON_PICKAXE:4.0D
    - DIAMOND_PICKAXE:5.0D
    - WOODEN_SHOVEL:1.0D
    - GOLDEN_SHOVEL:1.0D
    - STONE_SHOVEL:2.0D
    - IRON_SHOVEL:3.0D
    - DIAMOND_SHOVEL:4.0D

  # Settings related to features for AntiCooldown
  Features:
    # Should the SweepAttack be deactivated?
    # This also automatically disables any particles of an sweep attack
    # if ProtocolLib is installed.
    # Available options: true, false
    DisableSweepAttacks: true
    # Should the new attack sounds be deactivated?
    # Available options: true, false
    DisableNewCombatSounds: true
    CustomItemDamage:
      # Determines whether the EnableCustomItemDamage module should be activated.
      # The damage of the defined items in "CustomItemDamage" is thereby applied.
      # Available options: true, false
      EnableCustomItemDamage: false
      # Should a message in the form of an ActionBar be sent to the attacker?
      # Available options: true, false
      SendActionBar: true
    ItemRestriction:
      # Determines whether the item restrictions are to be used.
      # Available options: true, false
      EnableItemRestriction: false
      # Should a message be sent to the player in the form of an ActionBar
      # when their Cooldown status has changed due to a restricted item?
      # Available options: true, false
      SendActionBar: true
      # Determines whether the defined items are to be used as a whitelist.
      # The cooldown is only deactivated if this is the case.
      # Available options: true, false
      UseAsWhitelist: false
  Updates:
    # Should AntiCooldown check for updates?
    # Available options: true, false
    UseUpdateChecker: true
    # If there is an update, should this be output in the console?
    # Available options: true, false
    ConsoleNotify: true
    # If there is an update, should this be displayed to an admin when logging in?
    # Available options: true, false
    IngameNotify: true

# Version of the current config
# DO NOT CHANGE!
ConfigVersion: 9
```
