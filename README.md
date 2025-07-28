# at_hud

A modern, customizable FiveM HUD for ESX servers.

## Features
- Health, armor, hunger, and thirst bars
- Speedometer, fuel, minimap, seatbelt, and location display
- Color customization for all HUD elements
- Notification system integration (ox_lib, esx, custom)
- Configurable seatbelt key and built-in seatbelt system
- Clean, responsive React UI (NUI)
- Easy to integrate with custom scripts

## Configuration
All options are in `config/shared.lua`:
- Enable/disable HUD elements
- Set default colors for icons
- Choose notification system (`notify = 'ox_lib'` or `'esx'`)
- Choose fuel system (`fuelSystem = 'ox_fuel'` or `'legacyfuel'`)
- Set seatbelt key (`seatbeltKey = 'B'`)
- Enable/disable built-in seatbelt system (`useBuiltInSeatbelt = true/false`)

## Usage
1. Place the resource in your server's resources folder.
2. Configure `config/shared.lua` as needed.
3. Start the resource in your server.cfg: `ensure at_hud`
4. Use `/seatbelt` or your configured key to toggle the seatbelt.

## Integration
- All notifications and fuel logic are routed through config and public functions for easy integration.
- Exports are available for seatbelt status.

## Requirements
- ESX (latest)
- ox_lib (optional, for notifications)
- LegacyFuel or ox_fuel (optional, for fuel bar)

# Exports
The following exports are available for integration with other scripts:
- `exports['at_hud']:hideHud()`
  - Hides the HUD UI.
- `exports['at_hud']:showHud()`
  - Shows the HUD UI.

