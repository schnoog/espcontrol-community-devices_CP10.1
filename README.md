## Why the ....

This is my try to brinig my Elecrow Crowpanel  
CrowPanel Advanced 10.1inch ESP32-P4 HMI AI Display 1024x600 IPS  
Hardware verson 1.0 (only 1 data line to esphosted) to live with espcontrol-community-devices

## What I did

I followed the instructions listed on adding-a-device.md  
and it was Step7s turn


```bash
python3 community/scripts/assemble.py --skip-web
```

which in return welcomed me with

```bash
[assemble] Running generators ...
ERROR: product/v2/device_catalog.json failed validation:
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateCardIcon references unknown font id 'font_icon_card'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionTitle references unknown font id 'font_text_body'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionValue references unknown font id 'font_text_body'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.icon references unknown font id 'font_icon_main'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.largeSensor references unknown font id 'font_number_value_large'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaControlTitle references unknown font id 'font_cover_art_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtArtist references unknown font id 'font_cover_art_artist'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtTitle references unknown font id 'font_cover_art_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaTitle references unknown font id 'font_text_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.sensor references unknown font id 'font_number_value'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.subpageChevron references unknown font id 'font_icon_status'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeLabel references unknown font id 'font_text_large'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeNumber references unknown font id 'font_number_value_large'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_title_font references unknown font id 'font_cover_art_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_artist_font references unknown font id 'font_cover_art_artist'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_time_font references unknown font id 'font_cover_art_time'
[assemble]   Generator warning: 'python3 scripts/generate_device_manifest.py' exited with code 1
[assemble]   (Continuing — generator failure may require extra dependencies)
[assemble]   Generator warning: 'python3 scripts/generate_device_slots.py' exited with code 1
Traceback (most recent call last):
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/generate_device_slots.py", line 867, in <module>
    raise SystemExit(main())
                     ^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/generate_device_slots.py", line 838, in main
    for device in slot_devices():
                  ^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/product_schema.py", line 936, in slot_devices
    return load_slot_devices(path)
           ^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/device_profiles.py", line 993, in slot_devices
    return [slot_device(profile) for profile in load_device_profiles(path).values()]
                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/device_profiles.py", line 863, in load_device_profiles
    raise DeviceProfileError("\n".join(errors))
device_profiles.DeviceProfileError: crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateCardIcon references unknown font id 'font_icon_card'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionTitle references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionValue references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.icon references unknown font id 'font_icon_main'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.largeSensor references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaControlTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtArtist references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaTitle references unknown font id 'font_text_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.sensor references unknown font id 'font_number_value'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.subpageChevron references unknown font id 'font_icon_status'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeLabel references unknown font id 'font_text_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeNumber references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_title_font references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_artist_font references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_time_font references unknown font id 'font_cover_art_time'
[assemble]   (Continuing — generator failure may require extra dependencies)
[assemble]   Generator warning: 'python3 scripts/build.py devices' exited with code 1
Traceback (most recent call last):
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/build.py", line 4191, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/build.py", line 4160, in main
    dirty = sync_device_capabilities(check_only=check_only)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/build.py", line 3577, in sync_device_capabilities
    capabilities = public_device_capabilities()
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/device_profiles.py", line 1029, in public_device_capabilities
    profiles = load_device_profiles(path)
               ^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/device_profiles.py", line 863, in load_device_profiles
    raise DeviceProfileError("\n".join(errors))
device_profiles.DeviceProfileError: crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateCardIcon references unknown font id 'font_icon_card'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionTitle references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionValue references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.icon references unknown font id 'font_icon_main'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.largeSensor references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaControlTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtArtist references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaTitle references unknown font id 'font_text_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.sensor references unknown font id 'font_number_value'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.subpageChevron references unknown font id 'font_icon_status'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeLabel references unknown font id 'font_text_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeNumber references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_title_font references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_artist_font references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_time_font references unknown font id 'font_cover_art_time'
[assemble]   (Continuing — generator failure may require extra dependencies)
[assemble] Generators complete.
[assemble] Running validators ...
ERROR: product/v2/device_catalog.json failed validation:
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateCardIcon references unknown font id 'font_icon_card'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionTitle references unknown font id 'font_text_body'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionValue references unknown font id 'font_text_body'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.icon references unknown font id 'font_icon_main'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.largeSensor references unknown font id 'font_number_value_large'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaControlTitle references unknown font id 'font_cover_art_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtArtist references unknown font id 'font_cover_art_artist'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtTitle references unknown font id 'font_cover_art_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaTitle references unknown font id 'font_text_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.sensor references unknown font id 'font_number_value'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.subpageChevron references unknown font id 'font_icon_status'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeLabel references unknown font id 'font_text_large'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeNumber references unknown font id 'font_number_value_large'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_title_font references unknown font id 'font_cover_art_title'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_artist_font references unknown font id 'font_cover_art_artist'
  - crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_time_font references unknown font id 'font_cover_art_time'
[assemble]   Validator warning: 'python3 scripts/check_device_manifest.py' exited with code 1
[assemble]   (Continuing — validator may require extra dependencies)
[assemble]   Validator warning: 'python3 scripts/check_device_matrix.py' exited with code 1
::error::crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateCardIcon references unknown font id 'font_icon_card'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionTitle references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionValue references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.icon references unknown font id 'font_icon_main'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.largeSensor references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaControlTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtArtist references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaTitle references unknown font id 'font_text_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.sensor references unknown font id 'font_number_value'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.subpageChevron references unknown font id 'font_icon_status'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeLabel references unknown font id 'font_text_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeNumber references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_title_font references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_artist_font references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_time_font references unknown font id 'font_cover_art_time'
Traceback (most recent call last):
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/check_device_matrix.py", line 162, in <module>
    raise SystemExit(main())
                     ^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/check_device_matrix.py", line 156, in main
    test()
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/check_device_matrix.py", line 43, in test_release_matrix_shape
    matrix = run_ok(["release"])
             ^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/check_device_matrix.py", line 20, in run_ok
    assert code == 0, f"{args} exited {code}"
           ^^^^^^^^^
AssertionError: ['release'] exited 1
[assemble]   (Continuing — validator may require extra dependencies)
[assemble]   Validator warning: 'python3 scripts/check_device_profiles.py' exited with code 1
Traceback (most recent call last):
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/check_device_profiles.py", line 953, in <module>
    raise SystemExit(main())
                     ^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/check_device_profiles.py", line 917, in main
    profiles = load_device_profiles()
               ^^^^^^^^^^^^^^^^^^^^^^
  File "/home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/scripts/device_profiles.py", line 863, in load_device_profiles
    raise DeviceProfileError("\n".join(errors))
device_profiles.DeviceProfileError: crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateCardIcon references unknown font id 'font_icon_card'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionTitle references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.climateOptionValue references unknown font id 'font_text_body'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.icon references unknown font id 'font_icon_main'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.largeSensor references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaControlTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtArtist references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaCoverArtTitle references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.mediaTitle references unknown font id 'font_text_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.sensor references unknown font id 'font_number_value'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.subpageChevron references unknown font id 'font_icon_status'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeLabel references unknown font id 'font_text_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.fonts.volumeNumber references unknown font id 'font_number_value_large'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_title_font references unknown font id 'font_cover_art_title'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_artist_font references unknown font id 'font_cover_art_artist'
crowpanel-esp32-p4-adv-101-1024x600-v10: firmware.display.coverArt.cover_art_time_font references unknown font id 'font_cover_art_time'
[assemble]   (Continuing — validator may require extra dependencies)
[assemble] Some validators had issues (see above).
[assemble] Skipping web bundle build (--skip-web).
[assemble] Assembly complete. Tree is at .assembly/

```

Doing what I can best, ignoring it, I cded into and started the esphome compile

```bash

cd .assembly
esphome compile ../devices/crowpanel-esp32-p4-adv-101-1024x600-v10/esphome.yaml
...
...compile...compile....compile
...
┏━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓
┃ Memory Type/Section ┃ Used [bytes] ┃ Used [%] ┃ Remain [bytes] ┃ Total [bytes] ┃
┡━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩
│ External RAM        │      4386936 │     3.27 │      129830760 │     134217696 │
│    .text            │      2407776 │     1.79 │                │               │
│    .rodata          │      1978604 │     1.47 │                │               │
│    .init_array      │          292 │      0.0 │                │               │
│    .appdesc         │          256 │      0.0 │                │               │
│    .tbss            │            8 │      0.0 │                │               │
│ DIRAM               │       375206 │    65.09 │         201258 │        576464 │
│    .bss             │       289280 │    50.18 │                │               │
│    .text            │        63310 │    10.98 │                │               │
│    .data            │        22456 │      3.9 │                │               │
│    .noinit          │          160 │     0.03 │                │               │
│ HP core RAM         │          112 │     1.37 │           8080 │          8192 │
│    .data            │           60 │     0.73 │                │               │
│    .text            │           52 │     0.63 │                │               │
│ LP RAM              │           56 │     0.17 │          32712 │         32768 │
│    .force_slow      │           32 │      0.1 │                │               │
│    .rtc_reserved    │           24 │     0.07 │                │               │
└─────────────────────┴──────────────┴──────────┴────────────────┴───────────────┘
Total image size: 4472546 bytes (.bin may be padded larger)
RAM:   [=======   ]  65.1% (used 375206 bytes from 576464 bytes)
Flash: [======    ]  55.0% (used 4472546 bytes from 8126464 bytes)
INFO Creating factory.bin...
INFO Created: /home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/../devices/crowpanel-esp32-p4-adv-101-1024x600-v10/.esphome/build/cp-adv-101-1024x600-v10/build/firmware.factory.bin
INFO Created: /home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/../devices/crowpanel-esp32-p4-adv-101-1024x600-v10/.esphome/build/cp-adv-101-1024x600-v10/build/firmware.ota.bin
INFO Created: /home/volker/Development/smarthome/basedev/espcontrol/ecdtest/.assembly/../devices/crowpanel-esp32-p4-adv-101-1024x600-v10/.esphome/build/cp-adv-101-1024x600-v10/build/firmware.elf
INFO Build Info: config_hash=0x7dbcf1f0 build_time_str=2026-09-12 17:25:20 +0200
INFO Successfully compiled program.


```

and the compilation went successful.  
I uploaded it to my display and it booted, showing me the home-assistent connection screen (I provided the wifi credentials in my secrets.yaml for testing purposes, same with ota credentials...).

## What the problem?
I tried to use the web-config, but tesing the devide without corresponding entry in the main repo web doesn't work. So I used github-actions to create my own github page, calling it directly works. 

https://schnoog.github.io/espcontrol-community-devices/webserver/www.js?devicecrowpanel-esp32-p4-adv-101-1024x600-v10&v=dev&ui=77c76ea6b1cd

But I didn't find a way to change to js call to my own github repo page and so I'm stuck.

## How I tested the current file set


```bash

# I cloned the repo 
git clone git@github.com:lamiskin/espcontrol-community-devices.git ecdtest
cd ecdtest/
npm install
#ready for the failed test? I am
python3 community/scripts/assemble.py --skip-web
#and ready to ignore the failure
cd ../mydevice/
cp community/catalog-fragment.json ../ecdtest/community/catalog-fragment.json
cd devices/
cp -r crowpanel-esp32-p4-adv-101-1024x600-v10 ../../ecdtest/devices/
cd ../../ecdtest/.assembly/
#and now I compiled it
esphome compile ../devices/crowpanel-esp32-p4-adv-101-1024x600-v10/esphome.yaml 

```

