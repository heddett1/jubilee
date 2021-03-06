# Changelog

All changes between releases are tracked here.

## (UPCOMING) rel/jubilee_2.0.2 (in development now)

### Major Fixes/Updates from Jubilee 2.0.1
- [x] The frame is now Gates Pulley Compatible.
    - Either Genuine Gates pulleys or generic pulleys can be dropped into the machine. Note that Gates Pulleys are slightly taller, so shims and washers have been called out in the instructions to handle the height differences. Several printed parts have been adjusted, and they are called out below.
- [x] All Delrin Corner Plates are now 3D printed except the Motor Plates. (You can still use the laser-cut ones, but you may need to add shim.)
    - This is to to handle intercompatibility with Gates/Generic pulleys. The Gates pulleys require taller shoulder screws, so I've opted for thickening these parts instead of adding shim.
- [ ] Metal Motor Plates now have a counterbore feature on both motor plates
    - Both Motor Plates now have a counterbore feature to accommodate the thicker motor spacer. This change was driven by the geometry changes to make the Gates pulleys a drop-in replacement.
- [ ] CAD model now displays the aluminum crossbar instead of the 6mm carbon fiber one.
    - If you need to reference the carbon fiber crossbar, it is stored in a Solidworks configuration in the top level assembly.
- [ ] All three printed components that couple the bed to the frame have heat-set inserts
    - The springs now connect to this part with a solder terminal lug, just like how they are connected to the bed. This change makes these parts much easier to assemble.
- [ ] Instructions have been updated for the bed plate, right motor corner plate (and upgrade), Z axis assembly, and heat set insert list

### Shopping List Changes
- [ ] The 2.0.1 Y axis limit switch (Part Num: D2HW-BL201H) has been reverted to the original switch from 2.0 (Part Num: D2HW-C201H).
    - The original Right Motor Plate Spacer was too short to fully embed the Y axis switch, but resizing for the Gates pulley option added enough space to add the original switch in. Overall, reducing the unique part count makes the project easier to order and assemble.
- [ ] Bed Retension Springs are now a stock part from AliExpress
    - 2.0.1 (and before) had instructions for making your own springs out of spring stock. This is a TON of extra work for a part you can just buy.
- [ ] Bed Retension Clips are now a different type of Terminal Lug
    - The Keystone 7328 Terminal Lugs have been replaced by 4000 Terminal Lugs, which are much easier to bend around the spring. You will need 6 of them.
- [ ] 3 more M3 heat set inserts

### Updating from 2.0.1 to 2.0.2
If you would like to have the future option of updating to genuine Gates pulleys, the following part **must** be reprinted
- 4x [Printed Pulley Spacer]
- [Right Motor Plate Spacer](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/right_motor_corner_bracket_spacer.STL) RMS-04
- [Right Motor Plate](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/right_motor_plate.STL) RMP-04
- [Carriage Back Plate](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/toolchanger/toolchange_carriage/carriage_back_plate.STL) CBP-03
- [Left Crossbar Pulley Reinforcement Plate]
- [Right Crossbar Pulley Reinforcement Plate]
- [Left Corner Pulley Reinforcement Plate]
- [Right Corner Pulley Reinforcement Plate]

If you do not plan to update to genuine Gates pulleys, no changes need to be made from 2.0.1.

The following parts were tweaked for ease of assembly:
- [Fixed Half Pulley](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/toolchanger/toolchanger_locking_mechanism/fixed_half_pulley.STL) FXP-09
    - The hole for the 16mm long M3 screw is now slightly larger to make it easier to screw in.
- [Back Bed Coupler](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/back_bed_coupling_lift.STL) BBC-04
    - has a threaded heat-set insert
- [Front Left Bed Coupler](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/front_left_bed_coupling_lift.STL) LBC-04
    - has a threaded heat-set insert
- [Front Right Bed Coupler](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/front_right_bed_coupling_lift.STL) RBC-04
    - has a threaded heat-set insert
	
The following parts were tweaked for aesthetics:
- [Left Motor Plate Spacer](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/left_motor_corner_bracket_spacer.STL) LMS-04

## rel/jubilee_2.0.1 - Mar 10, 2020

### Major Fixes/Updates from 2.0
- The [Aluminum Crossbar](https://www.mandalaroseworks.com/jubilee/crossbar) is now available from Mandala Rose Works for $80. It is now the default in the BOM. Should you choose to upgrade from the carbon fiber crossbar, you will need to:
    - Print the latest [Right Motor Plate Spacer](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/right_motor_corner_bracket_spacer.STL)
    - Print the [X Limit Trigger](https://github.com/machineagency/jubilee/blob/master/frame/upgrades/aluminum_crossbar/fabrication_exports/stls/x_limit_trigger.STL)
    - purchase 1x M3, 10mm standoff from [McMaster-Carr](https://www.mcmaster.com/95947a006)
    - purchase 1x M3, 16mm buttonhead screw from [McMaster-Carr](https://www.mcmaster.com/92095a184) or [Bolt Depot](https://www.boltdepot.com/Product-Details.aspx?product=7222)
    - purchase 1x D2HW-BL201H from [Digikey](https://www.digikey.com/products/en?keywords=D2HW-BL201H)
    - Optional: replace the sixteen M3, 12mm buttonhead screws for bolting in the rail with M3, 10mm screws instead
- Adjusted Parking Post for the default extruder such that the tool doesn't twist while being picked up. Updated [assembly instructions](https://github.com/machineagency/jubilee/blob/master/tools/jubilee_tools/tool_posts/configurable_tool_post/assembly_instructions/parking_post_assembly_instructions.pdf)
- Adjusted the Carriage Back Plate and pulley spacers such that the nominal position of both belts is coplanar, rather than slightly off. Fixes [Issue #14](https://github.com/machineagency/jubilee/issues/14).
- swapped M3 nuts and for heat set inserts int the Carriage Back Plate to add clearance for the aluminum crossbar upgrade.
- Updated the instructions to show how to properly install the composite _Keep Nuts_ into the carbon fiber crossbar. Fixes [Issue #15](https://github.com/machineagency/jubilee/issues/15).
- Re-exported latest STL files for Extruder Tool
- Added an "Upgrades" folder for alternate frame components
- Tweaked direct drive extruder to fix compatibility issue when assembling for a V6 hotend.
- Adding Heatsinks to default extruder BOM for the stepper motors as they can get hot enough to warp the tool plates

The following parts *must* be reprinted since rel/jubilee-1.0:
- [Carriage Back Plate](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/toolchanger/toolchange_carriage/carriage_back_plate.STL)
- [Belt Clasp](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/belt_clasp.STL)
- [Printed Pulley Spacer](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/printed_pulley_spacer.STL)
- [Parking Post Base](https://github.com/machineagency/jubilee/blob/master/tools/jubilee_tools/tool_posts/configurable_tool_post/fabrication_exports/parking_post_base_47mm.STL)
- [Tool Holder](https://github.com/machineagency/jubilee/blob/master/tools/jubilee_tools/tool_posts/configurable_tool_post/fabrication_exports/tool_holder_47mm.STL)

The following parts were tweaked, but do not need to be reprinted if you have already assembled your machine.
- [Left Motor Plate Spacer](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/left_motor_corner_bracket_spacer.STL) has a bumper feature to make the y rails easier to install in a consistent spot.
- [Right Motor Plate Spacer](https://github.com/machineagency/jubilee/blob/master/frame/fabrication_exports/3d_printed_parts/frame/right_motor_corner_bracket_spacer.STL) has a bumper feature to make the y rails easier to install in a consistent spot.

### Minor Fixes/Tweaks
- Most printed parts now have part numbers with the revision id on them. This feature is useful for identifying what version of a part you have to decide whether you need to upgrade to a newer revision in the future
- Fixed old V1-related graphics in Remote Elastic Lock Instructions. Some photos are still out of date, but the whole is useable in its current state.
- Reorganized file structure to clearly separate tools from frame
- M3 Drop-in T nuts have been replaced with M3 Slide-in T nuts, which are cheaper and less of a hassle to install.
- Y axis limit switch was moved forward by 0.2mm to ensure that it clicks even on poorly printed parts.

## rel/jubilee-2.0 - Jan 15, 2020

### Added
- Jubilee V2, *Cubilee*
- New [Bill of Materials](https://docs.google.com/spreadsheets/d/1pRzBQxVzL9c4T9b1RrKvSjlSwJJhJ7NcbSV6iJUv0X0/edit?usp=sharing). All parts that were added, changed-in-size, or increased in value since the V1 BOM are highlighted in yellow.

### Changed
- Frame was adjusted to accommodate larger tools and a build volume of 300x300x300mm. Size update also fixes issue [#4](https://github.com/machineagency/jubilee/issues/4)
- Dowel pin spacing on the Coupling Plate was modified slightly to more easily lock E3D tool plates
- Back Panel bolt hole pattern now accommodates either a set of Duet2 + Duex5 boards or a set of Duet3 + 2 expansion boards + Raspi 
- Front opening has more clearance for bed plate removal 
- ZYLTech Leadscrews are now 375mm instead of 270mm
- Side Panel Sizes are slightly larger
- Back Panel Size is slightly larger
- Crossbar Size is slightly longer. New [DXF](https://github.com/machineagency/jubilee/blob/dev/jubilee_2.0/fabrication_exports/machined_parts/crossbar/crossbar_6mm_for_400mm_mgn12_rail.DXF)
- Belt lengths are now slightly longer
- X-axis MGN12 rail is now 400mm instead of 350mm
- Z-axis MGN12 rail is now 400mm instead of 300mm
- 3D Printed Feet are now easier to assemble and ~$30 cheaper
- Mounting plates for Z axis motors are now one piece each instead of two.
- All M2 Dowel Pins were replaced with set screws for easier assembly.
- Toolchanger Elastic Lock Actuator was redesigned for ease of assembly. Using a V1 lock will still work though
- The BOM lists the embedded magnet build plate as the default since it fixes issue [#3](https://github.com/machineagency/jubilee/issues/3)

The following parts *must* be reprinted since Release 1.0.0:
- [Front Left Bed Coupling Lift](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_left_bed_coupling_lift.STL)
- [Front Right Bed Coupling Lift](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_right_bed_coupling_lift.STL)
- [Front Left Z Motor Plate](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_left_z_motor_plate.STL)
- [Front Right Z Motor Plate](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_right_z_motor_plate.STL)
- [Back Z Motor Plate](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/back_z_motor_plate.STL)
- [Carriage Coupler Plate](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/toolchanger/toolchange_carriage/carriage_coupler_plate.STL)

The following parts have minor changes, but do not need to be reprinted:
- [Left Motor Corner Bracket Spacer](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/left_motor_corner_bracket_spacer.STL)
- [Right Motor Corner Bracket Spacer](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/right_motor_corner_bracket_spacer.STL)
- [Left Double Pulley Corner Bracket](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/left_double_pulley_corner_bracket.STL)
- [Right Double Pulley Corner Bracket](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/right_double_pulley_corner_bracket.STL)
- [Front Left Leadscrew Retainer](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_left_leadscrew_retainer.STL)
- [Front Right Leadscrew Retainer](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_right_leadscrew_retainer.STL)
- [Back Leadscrew Retainer](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/back_leadscrew_retainer.STL)
- [Back Bed Coupling Lift](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/back_bed_coupling_lift.STL)
- [Front Left Foot](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_left_foot.STL)
- [Front Right Foot](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/front_right_foot.STL)
- [Back Left Foot](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/back_left_foot.STL)
- [Back Right Foot](https://github.com/machineagency/jubilee/blob/master/fabrication_exports/3d_printed_parts/frame/back_right_foot.STL)

### Removed
- Delrin Slip Face on toolchanger elastic lock


## [1.0.0] - 2019-09-09

### Added
- Jubilee V1, *the original Jubilee*
- Original [Bill of Materials](https://docs.google.com/spreadsheets/d/1gq5yLxlfPtb3yrGsuXR_ZLhAFGB77CzGvfcWYyYIvT4/edit#gid=0)
