# Maps

My maps consist of :-

1. The backgroud is created from Openstreetmap data.
2. A GPX route file of the path to be followed.

The maps are  processed using Maperitive utilsing a custom set of rules.
The map is then exported as scalable vector graphic .svg file for further editing in Inkscape.

## Software

- Maperitive from <http://maperitive.net/>
- Inkscape from <https://inkscape.org/>

Read the tutorials <http://maperitive.net/docs/TwoMinutesIntro.html> and <http://maperitive.net/docs/TenMinutesIntro.html>

## Maperitive interactively

### Load the Background Map

1. Open Maperitive
2. Scroll and zoom the map to the required area.
3. Download the OSM data (Map > Download OSM Data )
4. In the Map Sources window, bottom right, de-select the Web map, custom rules are not applied to the web map.
5. Apply a set of rendering rules (Map > Switch to Rendering Rules)

### Load the Route

1. Import the gpx file for the route (File > Open Map Sources)

### Export the Map for futher processing

1. Select the export (Tools > Export to .....bitmap or svg)

## Maperitive using scripts

It is possible to create script files that contain all the information for producing maps, automating all the steps above :- loading map date, choosing a rendering rule-set, loading a route file and exporting a png or svg file. An example has been added to the Scripts folder.

## Customising Maperitive

### Custom Rulesets

The default rules files are available in `C:\Program Files\Maperitive\Rules`.

The files have the extension `.mrules`.

Copy the file and edit using a text editor. The Maperitive tutorials will give an overview of the structure and format of the ruleset files.

### Adding New Rulesets

1. Using the ruleset file you have available or edited.
2. Copy the `.mrules` file you want into the 'rules' folder within your maperitive installation (Windows default would be `C:\Program Files\Maperitive\Rules`).
3. Start Maperitive.
4. In the "Command Prompt" box at the bottom enter `use-ruleset location=rules\<RULEFILENAME>.mrules as-alias="<Rule Alias Name>"`
5. `<RULEFILENAME>.mrules` should be replaced with the actual filename of the rule file
6. `<Rule Alias Name>` should be replaced with the alias you want to appear in the rules list in Maperitive
7. `<index number>` is optional and should be replaced with an integer indicating where you want the alias to appear in the rule list
To have the ruleset available everytime you open Maperitive add the `use-ruleset` entry to  `C:\Program Files\Maperitive\Scripts\default.mscript`

## Map Data

Map data from Openstreet map <https://www.openstreetmap.org>

1. Select the Export tab, top left
2. Manually select an area.
3. Select the Export button. This should download a file map.osm
There are limits on the size of the files that can be downloaded from Openstreetmap or one of the other sources listed.
