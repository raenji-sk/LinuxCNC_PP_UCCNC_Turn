# LinuxCNC_PP_UCCNC_Turn

25.1.2024
Changes copared to Autodesk Official LCNC Turn PP:

1. Change output to radius mode G8, on X command and beginning of the gcode
  a. var xFormat = createFormat({decimals:(unit == MM ? 3 : 4), forceDecimal:true, scale:1}); // 1 - Radius mode, 2 - diameter mode
  b. writeBlock(gFormat.format(8)); // 7 -Diameter mode, 8 - Radius mode
2. Added G43 Hx tool offset when M6 tool change is present
3. Add passtrough for "comment" and "custom gcode" in F360
