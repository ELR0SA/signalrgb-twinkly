# Twinkly

[![Add To Installation](https://marketplace.signalrgb.com/resources/add-extension-256.png 'Add to My SignalRGB Installation')](signalrgb://addon/install?url=https://github.com/ELR0SA/signalrgb-twinkly)

## Getting started
This fork is based on SignalRGB's `boX-Development` branch and focuses on stable
real-time canvas streaming for Twinkly Wi-Fi devices.

## Tested devices

- TWFL300STW (288 active LEDs, firmware 2.10.0)
- TWQ064STW (576 active LEDs, firmware 2.9.1)

## Stability changes

- Uses the modern fragmented Gen 3 real-time protocol for current hardware,
  including firmware family `S` devices such as TWFL300STW.
- Refreshes authentication before the device's session expires.
- Restores `rt` mode after a lost connection or after another app takes control.
- Runs health checks asynchronously so a slow HTTP request does not block canvas
  rendering.
- Caps output at the controllers' advertised maximum of 40 FPS.
- Fixes 2D layout parsing and adds the TWFL300STW product image mapping.

## Known Issues
- No Support For First Generation Devices (Need Users with First Gen Devices)
- Second Gen Devices With Older Firmware Version May Require a Firmware Update.

## Custom addon installation

1. In SignalRGB, open the Twinkly device information page and click **Plugins**
   to open the custom plugins folder.
2. Copy `Twinkly.js` from this repository into that folder.
3. Restart SignalRGB so it reloads the addon.
4. Leave **Auto Reconnect** enabled and start with **Maximum Frame Rate** at 40.

SignalRGB custom plugins override bundled plugins and persist across application
updates. Remove the custom copy when you want to return to SignalRGB's bundled
Twinkly addon.

## Support
Feel free to open issues here, or join the SignalRGB Testing Server and post an issue there https://discord.com/invite/J5dwtcNhqC.
