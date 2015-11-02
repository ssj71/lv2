LV3 Wishlist
===

LV2 core has stablized but occasionally things arise that we wish had been done. This document exists to track those, especially design flaws that should be avoided should an LV3 ever arise.



* Plugin Struct
 * this should have been clasically extensible by just tacking on methods

* Connect Port function
 * this design isn't good, reqiring this function be called and pointers be given the plugin before every run().
 * better design would be to pass a double pointer to an array of ports something like run(const
 void** inputs, void*)

* Preset Banks
 * these should have been built into plugins so that presets are always contained in a bank
 * heirarcy should be plugin>banks>presets

