ephember
========================================

ephember is a Python module implementing an interface to the [EPH Control Systems Ember API](http://emberapp.ephcontrols.com/).  It allows a user to interact with their EPH heating system.

This code is cloned from the core home assistant [ephember component](https://github.com/home-assistant/core/tree/dev/homeassistant/components/ephember) and modified as documented below;

climate.py
========================================
1. Removed import of zone_is_hot_water and zone_target_temperature from pyephember.pyephember
2. Modified import of PLATFORM_SCHEMA, and included PRESET_BOOST plus PRESET_NONE from homeassistant.components.climate
3. Modified OPERATION_LIST to [HVACMode.AUTO, HVACMode.HEAT, HVACMode.OFF]
4. Modified PLATFORM_SCHEMA assignment to use new import as defined in 2.
5. Updated EPH_TO_HA_STATE to new Operation list in 3.

manifest.json
========================================
1. Set pyephember version required to 0.4.0 in requirements