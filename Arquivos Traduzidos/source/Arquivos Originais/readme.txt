Rebuild 3 English language files
Sarah Northway - sarahnorthway@gmail.com
Generated October 10 2015

See http://rebuildgame.com/mods.php#language for more info
Visit http://forums.rebuildgame.com or http://steamcommunity.com/app/257170/discussions/ to discuss
Contact sarahnorthway@gmail.com with questions

In Java properties format
# Lines starting with a hash # are comments, they will be ignored
Text string ids ending with _picture, _pictureColin, _icon should not be changed

en_*.properties are the original raw files with comments
english_all_template.properties contains all language strings in one file with _picture, _pictureColin, _icon removed
Rebuild_3_English.po / Rebuild_3_English.pot all strings converted to POEdit format

Strings can include up to three dynamic arguments: {1}, {2}, and {3}. These will be replaced by something else, eg the name of a pet, the number of zombies killed, the type of equipment found, or even a whole sentence.

Italics are done using _underscores_.

Line breaks are done using \n

Common dynamic content is shown with tags in square braces []:
[CityName] - name of the current city
[square] - whatever building is being discussed eg "police station"
[Square] - most tags can be auto-capitalized eg "Police station"
[squares] - pluralized eg "police stations", defined in en_squares.properties
[missioning] - actionText for every mission eg "scavenging" from en_missionTypes.properties
[Faction], [factionNoThe], [factionAdjective], [faction's] - eg "The Riffs", "Riffs", 
	"Riff", "the Riffs'" from en_factions.properties
[FactionLeader], [factionLeader's] - eg "Gustav" from en_factions.properties

[*one|two|three] will display a random one of the choices for flavor variation
	feel free to remove these and only translate one choice, or add your own variations

[one|two|three] (so long as "one" is not "g", "g2", or "p" see below)
	also picks a random one, but consistently picks the same index during an event
	eg "The [yellow|red|blue] dress was the color of [the sun|blood|the sky]"
	feel free to remove these or add your own variations

Up to 2 survivors and 1 faction leader can be mentioned in a text string
	[Name] > "Joe", [FormalName] > "Joe Collins", [Name] > "Joe's", [FormalName's] > "Joe Collins'"
	for the second survivor, use [Name2], [Name2's], [FormalName2's] etc
	[job], [Job], [job2], [Job2] - "engineer", "soldier" etc from en_snippets.properties
	
[g|MALE_TERM|FEMAL_TERM] will be "MALE_TERM" for a male survivor
	or "FEMALE_TERM" for female survivor, eg [g|he is handsome|she is pretty]
	use [g2|he|she] to refer to the 2nd survivor in an event
common gender rules are defined in en_rules.properties
	[his] [himself2] or [man] becomes "her" "herself" or "woman" for female survivors
	delete them and replace with your own eg [lui] [il] etc
	
common gender rules will automatically have "faction" prepended for faction leaders
	eg [factionHe], [FactionHe], or for your own rules [factionLui] [FactionIl] etc

[p|SINGULAR_TERM|PLURAL_TERM] will be "SINGULAR_TERM" if there is only one survivor
	or "PLURAL_TERM" for plural, eg: [p|my life|our lives]
common plural rules are defined in en_rules.properties
	[we] [us] [our] becomes "I" "me" "my" etc if reporting survivor is alone
	delete them and replace with your own eg [nous] [on] etc

[a] and [A] are replaced last and will become "an" if preceding a vowel
	eg "[a] [square]" will be "a police station" or "an apartment"
	feel free to ignore these if your language doesn't use them
	
tutorial uses extra tags:
	[numColins], [numFoodPerFarm], [numFood], [numColinsPerSuburb], [completionGoal], [morale]
	also [touch] and [tap] become "touch" or "tap" on mobile, "click" on pc
	