# gtres

Simple bash resistance calculator.

## Installation

Download gtres and put it in your $PATH. You could try this:

```bash
sudo curl -o /usr/local/bin/gtres https://raw.github.com/seanirby/gtres/master/gtres
sudo chmod o+x /usr/local/bin/gtres
```

## Usage

gtres is used by providing a sequential list of colors corresponding to a valid 4, 5, or 6 band resistor definition. 

The order of arguments shall consist of the significant figures followed by the multiplier, the tolerance, and finally the temperature coefficient. See (http://www.michaels-electronics-lessons.com/images/resistor-color-code-all.gif) .

Examples:
```bash
$ gtres ora ora red sil
3300 Ohms, +-10%
$ gtres bro bla bla bla gol
100 Ohms, +-5%
$ gtres red pur blu bla gol bro
276 Ohms, +-5%, 100 ppm
```

Valid color inputs are:
```bash
"bla" #Black
"bro" #Brown
"red" #Red
"ora" #Orange
"yel" #Yellow
"gre" #Green
"blu" #Blue
"pur" #Purple
"gra" #Gray
"whi" #White
"sil" #Silver
"gol" #Gold
```

## TODO
*	Add help text
* Expand input options. 
		E.g. "bla, "BLACK", "black", "bLaC" valid are valid inputs
* Prettify output. 
		E.g. "6 MOhms..." instead of "6000000 Ohms..."
* Validate that input resistor matches with an EIA standard resistor value.  Provide output warning if it doesn't
* Provide support for weird resistors like 0 ohm.