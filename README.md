# Reusable Blocks Common

This repository contains commonly used basic schematic building blocks along 
with reference PCB designs in most cases.

These are meant to be used/imported into other projects to allow fast and 
efficient design for new projects without reinventing the wheel every time.


## Dependencies

None! That's the great part about the common repo.

Just the default KiCAD v9 installation will contain everything needed to use
this repository without depending on external plugins or libraries.

## Helper Scripts

This section is for describing future usage of scripting tools to automate
testing and modification of reusable blocks.

## Categories 

These are the current categories covered by the common repo, feel free to 
suggest more.

```sh
├── ADC
├── battery_managment_systems
├── boost_converters
├── buck_converters
├── circuit_protection
├── DAC
├── motor_drivers_brushed
├── motor_drives_brushless
├── usb
├── passive_filters 
├── active_filters

9 directories
```



## Contributing

If you want to help out or offer a suggestion feel free to create a issue or
a discussion topic.

You can also open a pull request if there is a reusable block you want to add.

### Checklist for schematics

- [ ] The schematic fits into an existing category.
- [ ] The version of KiCAD used is the same as listed as the default.
- [ ] The schematic fits onto a single A0-A4 page.
- [ ] The page title is accurate to the purpose.
- [ ] Only built in components and footprints are used.
- [ ] All ingoing and outgoing connections are hierarchical labels(except drop-in blocks).
- [ ] No global labels are used.
- [ ] Schematic's pass the Electrical Rules Checker(E.R.C.).
- [ ] All component values should specify details such as:
    - Reference: R1
    - Value: 10k 1/8W
    - Reference: C1
    - Value: 0.1u 6.3V
- [ ] Text boxes and notes on sheets use default text sizes.
- [ ] If spice modeling is used, the component models need to be included.

### Checklist for documentation

- [ ] Documentation should be written in markdown or LaTeX.
- [ ] Contains a description section.
- [ ] Contains a Ratings section of maximum acceptable voltage/current.
- [ ] Contains a design recommendations section.
- [ ] Contains a layout recommendation section 2 & 4+ layer.

### Checklist for PCBs

Optional at the moment.


## License

It's under a BSD-3 license and you can pretty much do anything you want with
this and use it for commercial applications.

