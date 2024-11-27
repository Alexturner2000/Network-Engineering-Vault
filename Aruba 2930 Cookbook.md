Compatible SFPs
- 1G SFP SX (Fiber Multimode) - J4858D
- 1G SFP SX (Fiber Singlemode) - J4859D



---

Default login (from factory)
username `admin`
password `<no-password>`

Since its managed by Aruba Central, not much is really needed here. Just troubleshooting commands


```
show aruba-central
```

Adding new devices
1. Navigate to https://common.cloud.hpe.com/devices/inventory and add new devices by spreadsheet (or manual)
2. Make sure you have added the purchased license key for all the switches (one key for switches, one key for APs)
3. Once applied to the switch/ap, connect them directly to the ISP
4. It will show up under the default group in Aruba Central. Move it to its corresponding group to apply the default template.
5. Add the switch to the site
6. Rename the switch. Go to the `site` -> `devices` -> `switches` -> select the switch -> `device` > change group var hostname. This change will happen immediately
