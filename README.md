# VoronTrident-printerbuildproject
CU3D 2026-2027 printer build project. STLs need to be sliced in accordance with th voron print requirements and the Prusa Pro HT90 printer we are using.

## Git miscanellous
Clone the repository. From your terminal, type:
```bash
cd myFolder
git clone https://github.com/ichasepigeons/VoronTrident-printerbuildproject.git
```
The project should appear under myFolder.

### How to contribute
Make sure you `git pull` beforehand to avoid merge conflict if someone else is working together.

Make your changes locally, then:
```bash
git add file1 file2 file3
git commit -m "Commit title" -m "Commit description"
git push origin main
```

Alternatively, you can use the `add files via upload` function on github in browser.

## How to slice STLs
Once you have the Prusa Slicer installed, you should import this [config bundle](./prusa-pro-ht90-profiles/PrusaSlicer_config_bundle_for_voronproject.ini) in the app (File -> import -> import config bundle...). Check that the print settings align with what was stated in the [BoM](./VoronTridentFullSTLs/BoM Voron Trident.xlsx), which also contains **the full list of parts** and **quantity and any specification required for each part**.

Once sliced, export the GCODEs - keeping the automatic naming with the part's name, quantity, print time, and grams of materials used - and save it to the corresponding directory location under the GCODEs folder.

### notes
To keep parts identifiable when printed, it is best to only have one component (but can be of multiple quantity) per sliced plate. 

To keep track of which parts has been sliced and which not, it is best to follow the same directory structure for the GCODEs and STLs for easy comparison. Placeholder files can be deleted when something has been uploaded to that directory (they are initally created as git does not see empty directory).

Quantity and color of the part can be found in the [BoM](./VoronTridentFullSTLs/BoM Voron Trident.xlsx). 

Provisionally we have decided accent colours to be red, and the rest be black.

## Directory structure
Please keep / append to the directory structure reasonably:
```yaml
VoronTrident-printerbuildproject/
└── VoronTridentFullSTLs/
    └── ... # Files to be sliced
└── VoronTridentGCODES/
    └── ... # Sliced files ready to be printed
└── prusa-pro-ht90-profiles/
    └── PrusaSlicer_config_bundle_for_voronproject.ini # the config bundle to be used!!
    └── ... # Configuration files taken from the physical printer. used to generate the config bundle above
```

## Relevant links, STL source
- [https://vorondesign.com/voron_trident](https://vorondesign.com/voron_trident)
- [https://github.com/VoronDesign/Voron-Trident](https://github.com/VoronDesign/Voron-Trident)
- [https://github.com/VoronDesign/Voron-Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner)
- [Voron sourcing FAQ, eg. how many kg of filament is needed](https://docs.vorondesign.com/sourcing_faq.html)
