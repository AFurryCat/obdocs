<table>
	<tbody>
		<tr>
			<td>:warning:</td>
			<td align="center"><b><i>Minions are entirely virtual, and not in any way tradeable for real GP or real money. It's simulating the real game for fun. We strictly do not allow any bot users to break any of the official OSRS rules. </br>Read the rules here: <a href="https://www.oldschool.gg/oldschoolbot/rules">Old School Bot Rules</a></i></b></td>
			<td>:warning:</td>
		</tr>
	</tbody>
</table>

Minions are a feature in Old School Bot that let you simulate playing a virtual RuneScape account in Discord.
You control a minion, who you send out to do various tasks, like killing monsters for loot, completing clue scrolls, and training skills.
With the loot they get, you can craft items, sell them, and trade to other real players.

If you notice any mistakes or missing information in this page, you can [edit the page yourself](https://github.com/gc/obdocs/blob/master/minions.md), or report it to us via the [discord support server](https://discord.gg/ob)

# TODO: GENERATE CONTENTS PAGE

<i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generator</a></i>

# Getting started

Firstly, [read the rules](https://www.oldschool.gg/oldschoolbot/rules) and join the [Discord support server](https://discord.gg/ob).

We highly recommend joining the support server for multiple reasons:

- Bot updates are announced in the `#news` channel
- Help/Support available in the `#help-and-support` channel
- Buy/Sell items from other plays in the `#grand-exchange` channel
- Bot wide rare drops, pets etc announced in `#notifications` channel

## Activating your minion

The requirements to activate your minion vary depending upon the age of your Discord account, this is to guard against botting and alt accounts.

<table>
	<tbody>
		<tr>
			<th align="center">Discord account age</th>
			<th align="center">Minion creation requirements</th>
		</tr>
		<tr>
			<td align="center">Under 1 Month</td>
			<td align="center">Unable to create a minion.</td>
		</tr>
		<tr>
			<td align="center">1 - 6 Months</td>
			<td align="center">Requires 20m gp to create your minion.</td>
		</tr>
		<tr>
			<td align="center">6+ Months</td>
			<td align="center">No requirements.</td>
		</tr>
	</tbody>
</table>

You can use the `+daily` command every 12 hours to earn the required gp, this will ask you trivia questions and provide gp and special Diango items as a reward.
Becoming a [patron](https://www.patreon.com/oldschoolbot) allows you to bypass the above restrictions.

You can activate your minion by using the `+minion buy` command, or `+m buy` for short.

## Trips

TODO: Explain the concept of a trip and how patron can extend the trip time

## Banking

Your minion has a bank just like in the real game, loot from killing monsters and bosses will automatically be added to your bank along with raw crafting materials you gather and any items you make from them.

To view your bank use `+bank` or `+b` for short.

Once your bank grows large enough it will not all fit on the single bank page returned by the above command. This will be shown by the message at the top showing `Page 1 of x` when you run the command.

To see the next page simply add the page number onto the main bank command, for example `+bank 2`.

To see your entire bank in one image you can use the `+bank --full` command.

You can also view a text version of your bank using `+bank --text`. This will generate an output and then add emote reactions below it, these can be used to navigate between pages on the text bank. You will need to add a reaction for it to be registered, and then remove it and add again to register the second of that interaction. The emote reactions are monitored by the bot for **TODO: Clarify working of bot monitoring emotes to navigate**

### Searching

There are multiple ways to search your bank.

`+bank air rune` will search your bank specifically for `air rune` and return the quantity if found. The text must be an exact match including punctuation for this method to find the item.

`+bank --search=rune` will search your bank for `rune` using wildcards either side of it. So this example would match all magic runes as well as runite items.

**TODO: Add other search command options**

### Filtering

You can filter the output of the `+bank` command to show items relating to certain monsters/skills. To do this you add `--[filter]` to the end of any `+bank` command, including searches.

<table>
	<tbody>
		<tr>
			<th align="center">Monster</th>
			<th align="center">Skills</th>
			<th align="center">Items</th>
			<th align="center">Minigames</th>
		</tr>
		<tr>
			<td>
				<ul>
					<code>--barrows</code></br>
					<code>--cerb</code></br>
					<code>--corp</code></br>
					<code>--dks</code></br>
					<code>--gwd</code></br>
					<code>--kq</code></br>
					<code>--vorkath</code>
				</ul>
			</td>
			<td>
				<ul>
					<code>--agility</code></br>
					<code>--farming</code></br>
					<code>--fletching</code></br>
					<code>--herblore</code></br>
					<code>--prayer</code></br>
					<code>--skilling</code>
				</ul>
			</td>
			<td>
				<ul>
					<code>--food</code></br>
					<code>--herbs</code></br>
					<code>--potions</code>
				</ul>
			</td>
			<td>
				<ul>
					<code>--wt</code>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

# Skilling

Currently available skills are:

- [Agility](https://www.oldschool.gg/oldschoolbot/minions?Agility)
- [Cooking](https://www.oldschool.gg/oldschoolbot/minions?Cooking)
- [Crafting](https://www.oldschool.gg/oldschoolbot/minions?Crafting)
- [Firemaking](https://www.oldschool.gg/oldschoolbot/minions?Firemaking)
- [Fishing](https://www.oldschool.gg/oldschoolbot/minions?Fishing)
- [Fletching](https://www.oldschool.gg/oldschoolbot/minions?Fletching)
- [Mining](https://www.oldschool.gg/oldschoolbot/minions?Mining)
- [Prayer](https://www.oldschool.gg/oldschoolbot/minions?Prayer)
- [Runecrafting](https://www.oldschool.gg/oldschoolbot/minions?Runecrafting)
- [Smithing](https://www.oldschool.gg/oldschoolbot/minions?Smithing)
- [Woodcutting](https://www.oldschool.gg/oldschoolbot/minions?Woodcutting)

## Agility

You can train Agility using the `+laps` command.

`+laps <course command>` will do as many laps as possible for the given course in the trip.

`+laps 10 <course command>` will do 10 laps of the given course, and the trip will only take as long as needed to do those 10 laps.

### Courses

<table>
	<tbody>
		<tr>
			<th align="center">Agility Level</th>
			<th align="center">Course</th>
			<th align="center">Alias</th>
			<th align="center">Lap Time</th>
			<th align="center">Completion experience</th>
			<th align="center">Mark of Grace chance</th>
		</tr>
		<tr>
			<td align="center">1</td>
			<td align="center">Gnome Stronghold</td>
			<td align="center">
				<code>gnome stronghold</code></br>
				<code>gnome</code>
			</td>
			<td align="center">34 seconds</td>
			<td align="center">88</td>
			<td align="center">0%</td>
		</tr>
		<tr>
			<td align="center">10</td>
			<td align="center">Draynor Village</td>
			<td align="center">
				<code>draynor</code>
			</td>
			<td align="center">43 seconds</td>
			<td align="center">120</td>
			<td align="center">14.4%</td>
		</tr>
		<tr>
			<td align="center">20</td>
			<td align="center">Al Kharid</td>
			<td align="center">
				<code>al kharid</code>
			</td>
			<td align="center">65 seconds</td>
			<td align="center">180</td>
			<td align="center">14.4%</td>
		</tr>
		<tr>
			<td align="center">30</td>
			<td align="center">Varrock</td>
			<td align="center">
				<code>varrock</code>
			</td>
			<td align="center">66 seconds</td>
			<td align="center">238</td>
			<td align="center">22%</td>
		</tr>
		<tr>
			<td align="center">40</td>
			<td align="center">Canafis</td>
			<td align="center">
				<code>canafis</code>
			</td>
			<td align="center">75 seconds</td>
			<td align="center">240</td>
			<td align="center">39.5%</td>
		</tr>
		<tr>
			<td align="center">50</td>
			<td align="center">Falador</td>
			<td align="center">
				<code>falador</code></br>
				<code>fally</code>
			</td>
			<td align="center">58 seconds</td>
			<td align="center">440</td>
			<td align="center">21%</td>
		</tr>
		<tr>
			<td align="center">60</td>
			<td align="center">Seers Village</td>
			<td align="center">
				<code>seers village</code></br>
				<code>seers</code>
			</td>
			<td align="center">44 seconds</td>
			<td align="center">570</td>
			<td align="center">14.8%</td>
		</tr>
		<tr>
			<td align="center">70</td>
			<td align="center">Pollnivneach</td>
			<td align="center">
				<code>pollnivneach</code></br>
				<code>pol</code>
			</td>
			<td align="center">61 seconds</td>
			<td align="center">890</td>
			<td align="center">15.3%</td>
		</tr>
		<tr>
			<td align="center">80</td>
			<td align="center">Rellekka</td>
			<td align="center">
				<code>rellekka</code></br>
				<code>rel</code>
			</td>
			<td align="center">51 seconds</td>
			<td align="center">780</td>
			<td align="center">19.8%</td>
		</tr>
		<tr>
			<td align="center">90</td>
			<td align="center">Ardougne</td>
			<td align="center">
				<code>ardougne</code></br>
				<code>ardy</code>
			</td>
			<td align="center">45.6 seconds</td>
			<td align="center">793</td>
			<td align="center">30.4%</td>
		</tr>
	</tbody>
</table>

## Marks of Grace

Completing a lap of an agility course gives the possibility of being rewarded with a Mark of Grace. Marks of Grace can be used to create the Graceful Set.

TODO: Link graceful set to graceful set in item creation

## Benefits

Training your minions agility provides the following benefits

<table>
	<tbody>
		<tr>
			<th align="center">Skill</th>
			<th align="center">Agility Level</th>
			<th align="center">Benefit</th>
		</tr>
		<tr>
			<td align="center" rowspan="2">Runecrafting</td>
			<td align="center">60+</td>
			<td align="center">5% Boost</td>
		</tr>
		<tr>
			<td align="center">90+</td>
			<td align="center">10% Boost</td>
		</tr>
	</tbody>
</table>

## Cooking

You can train Cooking using `+cook [quantity] <food>`, for example `+cook 50 bass`.

You can boost Cooking xp rates when attempting to cook fish while having the cooking guantlets equipped which decrease your faliure rate when cooking fish.

### Courses

<table>
	<tbody>
		<tr>
			<th align="center">Cooking Level</th>
			<th align="center">Food</th>
			<th align="center">Experience Given</th>
			<th align="center">Burn Level</th>
		</tr>
		<tr>
			<td align="center" rowspan="5">1</td>
			<td align="center">Beef</td>
			<td align="center">30</td>
			<td align="center">31</td>
		</tr>
		<tr>
			<td align="center">Shrimps</td>
			<td align="center">30</td>
			<td align="center">34</td>
		</tr>
		<tr>
			<td align="center">Chicken</td>
			<td align="center">30</td>
			<td align="center">34</td>
		</tr>
		<tr>
			<td align="center">Anchovies</td>
			<td align="center">30</td>
			<td align="center">34</td>
		</tr>
		<tr>
			<td align="center">Sardine</td>
			<td align="center">40</td>
			<td align="center">37</td>
		</tr>
		<tr>
			<td align="center">5</td>
			<td align="center">Herring</td>
			<td align="center">50</td>
			<td align="center">41</td>
		</tr>
		<tr>
			<td align="center">10</td>
			<td align="center">Mackerel</td>
			<td align="center">60</td>
			<td align="center">45</td>
		</tr>
		<tr>
			<td align="center">15</td>
			<td align="center">Trout</td>
			<td align="center">70</td>
			<td align="center">49</td>
		</tr>
		<tr>
			<td align="center">18</td>
			<td align="center">Cod</td>
			<td align="center">75</td>
			<td align="center">52</td>
		</tr>
		<tr>
			<td align="center">20</td>
			<td align="center">Pike</td>
			<td align="center">80</td>
			<td align="center">64</td>
		</tr>
		<tr>
			<td align="center">25</td>
			<td align="center">Salmon</td>
			<td align="center">90</td>
			<td align="center">58</td>
		</tr>
		<tr>
			<td align="center" rowspan="2">30</td>
			<td align="center">Tuna</td>
			<td align="center">100</td>
			<td align="center">63</td>
		</tr>
		<tr>
			<td align="center">Karambwan</td>
			<td align="center">190</td>
			<td align="center">99</td>
		</tr>
		<tr>
			<td align="center">35</td>
			<td align="center">Jug of Wine</td>
			<td align="center">200</td>
			<td align="center">68</td>
		</tr>
		<tr>
			<td align="center">40</td>
			<td align="center">Lobster</td>
			<td align="center">120</td>
			<td align="center">74</td>
		</tr>
		<tr>
			<td align="center">43</td>
			<td align="center">Bass</td>
			<td align="center">130</td>
			<td align="center">80</td>
		</tr>
		<tr>
			<td align="center">45</td>
			<td align="center">Swordfish</td>
			<td align="center">140</td>
			<td align="center">86</td>
		</tr>
		<tr>
			<td align="center">62</td>
			<td align="center">Monkfish</td>
			<td align="center">150</td>
			<td align="center">90</td>
		</tr>
		<tr>
			<td align="center">80</td>
			<td align="center">Shark</td>
			<td align="center">210</td>
			<td align="center">99</td>
		</tr>
		<tr>
			<td align="center">84</td>
			<td align="center">Anglerfish</td>
			<td align="center">230</td>
			<td align="center">99</td>
		</tr>
		<tr>
			<td align="center">90</td>
			<td align="center">Dark crab</td>
			<td align="center">215</td>
			<td align="center">99</td>
		</tr>
		<tr>
			<td align="center">91</td>
			<td align="center">Manta ray</td>
			<td align="center">216.2</td>
			<td align="center">99</td>
		</tr>
	</tbody>
</table>

### Useful Items

#### Cooking Gauntlets

Reduce the burn level of certain foods. TODO: Reference questing to obtain

<table>
	<tbody>
		<tr>
			<th align="center">Food</th>
			<th align="center">Burn Level When Wearing</th>
		</tr>
		<tr>
			<td align="center">Lobster</td>
			<td align="center">74</td>
		</tr>
		<tr>
			<td align="center">Swordfish</td>
			<td align="center">81</td>
		</tr>
		<tr>
			<td align="center">Monkfish</td>
			<td align="center">88</td>
		</tr>
		<tr>
			<td align="center">Shark</td>
			<td align="center">94</td>
		</tr>
		<tr>
			<td align="center">Anglerfish</td>
			<td align="center">98</td>
		</tr>
	</tbody>
</table>

# Combat

TODO: Explain how to kill a monster
TODO: Explain how % buff items work (reduce trip time)
TODO: Link all items to how to obtain them

## Monsters

## Bosses
<a href="#Barrows">Barrows</a></br>
<a href="#Callisto">Callisto</a></br>
<a href="#Cerberus">Cerberus</a></br>
<a href="#ChaosElemental">Chaos Elemental</a></br>
<a href="#ChaosFanatic">Chaos Fanatic</a></br>
<a href="#CommanderZilyana">Commander Zilyana</a></br>
<a href="#CorporealBeast">Corporeal Beast</a></br>
<a href="#CrazyArchaeologist">Crazy Archaeologist</a></br>
<a href="#DagannothPrime">Dagannoth Prime</a></br>
<a href="#DagannothRex">Dagannoth Rex</a></br>
<a href="#DagannothSupreme">Dagannoth Supreme</a></br>
<a href="#GeneralGraardor">General Graardor</a></br>
<a href="#GiantMole">Giant Mole</a></br>
<a href="#KrilTsutsaroth">K'ril Tsutsaroth</a></br>
<a href="#KalphiteQueen">Kalphite Queen</a></br>
<a href="#KingBlackDragon">King Black Dragon</a></br>
<a href="#Kreearra">Kree'arra</a></br>
<a href="#LizardmanShaman">Lizardman Shaman</a></br>
<a href="#Scorpia">Scorpia</a></br>
<a href="#Venenatis">Venenatis</a></br>
<a href="#Vetion">Vet'ion</a></br>
<a href="#Vorkath">Vorkath</a></br>
<a href="#Zulrah">Zulrah</a>

<hr />

### <a name="Barrows">Barrows</a>
#### Alias
`barrows`
#### Notable Loot
Torag's Armour Components</br>
Guthan's Armour Components</br>
Karil's Armour Components</br>
Ahrim's Armour Components</br>
Dharok's Armour Components</br>
Verac's Armour Components</br>
<a href="https://oldschool.runescape.wiki/w/Barrows#Rewards">Full Loot Table</a>
#### Kill Requirements
##### Skills
Prayer: 43+
#### Boost Items
+2% Barrows Gloves</br>
+5% Iban's Staff

<hr />

### <a name="Callisto">Callisto</a>
#### Alias
`callisto`
#### Notable Loot
Dragon Pickaxe</br>
Tyrannical ring</br>
<a href="https://oldschool.runescape.wiki/w/Callisto#Drops">Full Loot Table</a>
#### Kill Requirements
##### Weapons / Armour
Helm: Verac's Helm</br>
Chest: Verac's Brassard</br>
Legs: Verac's Plateskirt</br>
Weapon: Verac's Flail
#### Boost Items
+2% Barrows Gloves</br>
+2% Berserker Ring

<hr />

### <a name="Cerberus">Cerberus</a>
#### Alias
`cerberus`, `cerb`
#### Notable Loot
Eternal crystal</br>
Pegasian crystal</br>
Primordial crystal</br>
Smouldering stone</br>
<a href="https://oldschool.runescape.wiki/w/Cerberus#Drops">Full Loot Table</a>
#### Kill Requirements
##### Skills
Prayer: 43+
##### Weapons / Armour
Chest: Torag's Platebody or Dharok's Platebody or Bandos Chestplate</br>
Legs: Torag's Platelegs or Dharok's Platelegs or Bandos Tassets</br>
Weapon: Zamorakian Spear
#### Boost Items
+5% Bandos Chestplate</br>
+5% Bandos Tassets</br>
+10% Spectral Spirit Shield

<hr />

### <a name="ChaosElemental">Chaos Elemental</a>
#### Alias
`chaos elemental`, `chaos ele`, `chaos el`
#### Notable Loot
Dragon Pickaxe</br>
<a href="https://oldschool.runescape.wiki/w/Chaos_Elemental#Drops">Full Loot Table</a>
#### Kill Requirements
##### Weapons / Armour
Chest: Karil's Leathertop or Black D'hide Body</br>
Legs: Karil's Leatherskirt or Black D'hide Chaps
#### Boost Items
+3% Archers Ring</br>
+3% Barrows Gloves

<hr />

### <a name="ChaosFanatic">Chaos Fanatic</a>
#### Alias
`chaos fanatic`, `fanatic`
#### Notable Loot
Odium Shard 1</br>
<a href="https://oldschool.runescape.wiki/w/Chaos_Fanatic#Drops">Full Loot Table</a>
#### Kill Requirements
None
#### Boost Items
+3% Karil's Leathertop</br>
+3% Karil's Leatherskirt

<hr />

### <a name="CommanderZilyana">Commander Zilyana</a>
#### Alias
`commander zilyana`, `saradomin`, `zilyana`, `sara`, `zily`
#### Notable Loot
`Armadyl crossbow`</br>
`Godsword Shard 1, 2 and 3`</br>
`Saradomin Sword`</br>
`Saradomin Hilt`</br>
<a href="https://oldschool.runescape.wiki/w/Commander_Zilyana#Drops">`Full Loot Table`</a>
#### Kill Requirements
<b><i>Skills</i></b></br>
`Agility:` 70+</br>
`Prayer:` 43+
</br><b><i>Quest Points</i></b></br>
75+
</br><b><i>Weapons / Armour</i></b></br>
`Chest`: Armadyl Chestplate or Karil's Leathertop</br>
`Legs`: Armadyl Chainskirt or Karil's Leatherskirt
#### Boost Items
`+5%` Armadyl Crossbow</br>
`+5%` Ranger Boots

<hr />

### <a name="CorporealBeast">Corporeal Beast</a>
#### Alias
`corporeal beast`, `corp`
#### Notable Loot
Arcane sigil</br>
Elysian sigil</br>
Holy elixir</br>
Spectral sigil</br>
Spirit shield
<a href="https://oldschool.runescape.wiki/w/Corporeal_Beast#Drops">Full Loot Table</a>
#### Kill Requirements
##### Skills
Prayer: 43+
##### Weapons / Armour
Weapon: Zamorakian Spear
#### Boost Items
+5% Bandos Godsword</br>
+10% Dragon Warhammer


### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items


### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items


### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items

### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items


### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items



### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items


### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items


### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items



### <a name=""></a>
#### Alias
#### Notable Loot
<a href="">Full Loot Table</a>
#### Kill Requirements
##### Skills
##### Quest Points
##### Weapons / Armour
#### Boost Items

.

.

.

.

.

.

![https://i.imgur.com/hZUNtgK.png](https://i.imgur.com/hZUNtgK.png)| Corporeal Beast

![https://i.imgur.com/eqvQC4C.png](https://i.imgur.com/eqvQC4C.png)| Crazy Archaeologist

![https://i.imgur.com/JfpXrXW.png](https://i.imgur.com/JfpXrXW.png)| Dagannoth Prime

![https://i.imgur.com/pO822rj.png](https://i.imgur.com/pO822rj.png)| Dagannoth Rex

![https://i.imgur.com/FKVIKMX.png](https://i.imgur.com/FKVIKMX.png)| Dagannoth Supreme

![https://i.imgur.com/sLdtsrg.png](https://i.imgur.com/sLdtsrg.png)| General Graardor

![https://i.imgur.com/igxsuRU.png](https://i.imgur.com/igxsuRU.png)| Giant Mole

![https://i.imgur.com/gVIOuaQ.png](https://i.imgur.com/gVIOuaQ.png)| K'ril Tsutsaroth

![https://i.imgur.com/rvqU0Z3.gif](https://i.imgur.com/rvqU0Z3.gif)| Kalphite Queen

![https://i.imgur.com/pQFbspB.png](https://i.imgur.com/pQFbspB.png)| King Black Dragon

![https://i.imgur.com/OfsrIfN.png](https://i.imgur.com/OfsrIfN.png)| Kree'arra

![https://i.imgur.com/Hv6IcBx.gif](https://i.imgur.com/Hv6IcBx.gif)| Lizardman Shaman

![https://i.imgur.com/iwGwt1F.png](https://i.imgur.com/iwGwt1F.png)| Scorpia

![https://i.imgur.com/HHEZj9X.png](https://i.imgur.com/HHEZj9X.png)| Venenatis

![https://i.imgur.com/iSWr25X.gif](https://i.imgur.com/iSWr25X.gif)| Vet'ion

![https://i.imgur.com/w9PrhyH.png](https://i.imgur.com/w9PrhyH.png)| Vorkath

![https://i.imgur.com/p6d3Wna.gif](https://i.imgur.com/p6d3Wna.gif)| Zulrah

# Boss and Monster Requirements

| **Boss**          | **QP required** |                                                               **Gear required**                                                               | **Skill(s) required** |
| ----------------- | :-------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------: |
| Barrows           |       N/A       |                                                                      N/A                                                                      |       43 Prayer       |
| Lizardman shaman  |       30        |                                                                Karils Crossbow                                                                |       43 Prayer       |
| Zulrah            |       75        |                                Armadyl chestplate, Armadyl chainskirt, Ahrim's robetop, and Ahrim's robeskirt                                 |       43 Prayer       |
| Vorkath           |       205       |                                                    Armadyl chestplate, Armadyl chainskirt                                                     |       43 Prayer       |
| Giant Mole        |       N/A       |                                                               Full Dharok's set                                                               |       43 Prayer       |
| Callisto          |       N/A       |                                                               Full Verac's set                                                                |          N/A          |
| Venenatis         |       N/A       |                                                               Full Verac's set                                                                |          N/A          |
| King Black Dragon |       N/A       |                                                              Anti-Dragon shield                                                               |          N/A          |
| Chaos Elemental   |       N/A       |                            Karil's leathertop or Black d'hide body and Karil's leatherskirt or Black d'hide chaps                             |          N/A          |
| Corporeal Beast   |       N/A       |                                                               Zamorakian spear                                                                |       43 Prayer       |
| Cerberus          |       N/A       | Bandos chestplate or Torag's platebody or Dharok's platebody, Bandos tassets or Torag's platelegs or Dharok's platelegs, and Zamorakian spear |       43 Prayer       |
| Commander Zilyana |       75        |                            Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                            | 43 Prayer, 70 Agility |
| General Graardor  |       75        |                                                                      N/A                                                                      |       43 Prayer       |
| Kree'Arra         |       75        |                            Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                            |       43 Prayer       |
| K'ril Tsutsaroth  |       75        |                            Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                            |       43 Prayer       |
| Kalphite Queen    |       N/A       |                                 Verac's flail, Karil's leathertop or Black d'hide top, and Verac's plateskirt                                 |       43 Prayer       |
| Dagannoth Prime   |       N/A       |                    Full Guthan's, Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                     |       43 Prayer       |
| Dagannoth Rex     |       N/A       |                        Full Guthan's, Bandos chestplate or Torag's chestplate, and Bandos tassets or Torag's platelegs                        |       43 Prayer       |
| Dagannoth Supreme |       N/A       |                        Full Guthan's, Bandos chestplate or Torag's chestplate, and Bandos tassets or Torag's platelegs                        |       43 Prayer       |

## Fishing

You can train Fishing using `+fish [quantity] <fish>`, for example `+fish 100 lobster`.

Fishing bait is buyable with `+buy fishing bait`.

Dark fishing bait and Raw Karambwanji aren't sold by the bot and can be obtained by buying from other players or obtaining them yourself.

### Fish

| **Fish**          | **Required level** |
| ----------------- | :----------------: |
| Raw Shrimp        |         1          |
| Raw Sardine       |         5          |
| Raw Karambwanji   |         5          |
| Raw Herring       |         10         |
| Raw Anchovies     |         15         |
| Raw Mackerel      |         16         |
| Raw Trout         |         20         |
| Raw Cod           |         23         |
| Raw Pike          |         25         |
| Raw Salmon        |         30         |
| Raw Tuna          |         35         |
| Raw Lobster       |         40         |
| Raw Bass          |         46         |
| Barbarian fishing |         48         |
| Raw Swordfish     |         50         |
| Raw Monkfish      |         62         |
| Raw Karambwan     |         65         |
| Raw Shark         |         76         |
| Raw Anglerfish    |         82         |
| Raw Dark crab     |         85         |

- **Karambwanji**(Not to be mistaken for **Karambwan**) requires **15** Quest Points to fish.
- **Monkfish** requires **100** Quest Points to fish.
- **Anglerfish** requires **40** Quest Points to fish.

Click [here](https://i.imgur.com/0PUaA3J.png) for **Fishing** XP rates.

## Mining

You can train Mining using `+mine [quantity] <ore>`, for example `+mine 10 coal`.

Some ores reward you with golden nuggets or unidentified minerals.<br>
You can use nuggets to buy the prospector equipment and minerals to buy the three types of mining gloves.

If you have at least level 61, you can get one of these boosts to mining output from owning one of these pickaxes:

- Dragon pickaxe = +6%
- Infernal pickaxe = +10%
- Gilded pickaxe = +11%
- 3rd age pickaxe = +12%

You can also recieve boosts to mining xp rates from:

- Prospector's Outfit = +2.5%

  - Prospector's Helmet = +0.4%
  - Prospector's Jacket = +0.8%
  - Prospector's Legs = +0.6%
  - Prospector's Boots = +0.2%

- Mining Gloves
  - Mining Gloves = +2%
  - Superior Mining Gloves = +4%
  - Expert Mining Gloves = +6%

### Ores

| **Ore Name**   | **Nuggets** | **Minerals** | Required level\*\* |
| -------------- | :---------: | :----------: | :----------------: |
| Rune essence   |             |              |         1          |
| Copper ore     |             |              |         1          |
| Tin ore        |             |              |         1          |
| Iron ore       |             |              |         15         |
| Silver ore     |             |              |         20         |
| Pure essence   |             |              |         30         |
| Coal           |             |      ✔       |         30         |
| Gold ore       |      ✔      |              |         40         |
| Mithril ore    |      ✔      |              |         55         |
| Adamantite ore |      ✔      |              |         70         |
| Runite ore     |      ✔      |              |         85         |
| Amethyst       |             |      ✔       |         92         |

Click [here](https://i.imgur.com/b3HNdSi.png) for **Mining** XP rates.

## Smithing

You can train Smithing using `+smith` & `+smelt`
`+smelt [quantity] <bar>`, for example `+smelt 50 bronze bar`
`+smith [quantity] <item>`, for example `+smith adamant dart tips`

Smithing is one of the more useful skills on the bot, because it is required to create Godswords and such!

You can recieve a boost to gold bar smelting xp rates by equipping the goldsmith guantlets which increases the xp/bar from 22.5 to 56.2.

### Bars

| **Bar**    | **Required level** | **Materials needed**    |
| ---------- | :----------------: | ----------------------- |
| Bronze     |         1          | Tin + Copper            |
| Iron       |         15         | Iron ore                |
| Silver     |         20         | Silver ore              |
| Steel      |         30         | Iron ore + 2 coal       |
| Gold       |         40         | Gold ore                |
| Mithril    |         50         | Mithril ore + 4 coal    |
| Adamantite |         70         | Adamantite ore + 6 coal |
| Runite     |         85         | Runite ore + 8 coal     |

Click [here](https://i.imgur.com/tOTEqHS.png) for **Smithing** XP rates.

## Woodcutting

You can train Woodcutting using `+chop [quantity] <logs>`, for example `+chop 50 willow`.

If you have at least level 61, you can get one of these boosts from owning one of these axes:

- Dragon axe 9%
- Infernal axe 11%
- Gilded axe 12%
- 3rd age axe 13%

### Logs

| **Log**          | **Required level** |
| ---------------- | :----------------: |
| Logs             |         1          |
| Oak              |         15         |
| Willow           |         30         |
| Teak             |         35         |
| Maple            |         45         |
| Bark             |         45         |
| Mahogany         |         50         |
| Arctic pine logs |         42         |
| Yew              |         60         |
| Sulliusceps      |         65         |
| Magic            |         75         |
| Redwood          |         90         |

- **Sulliusceps** requires **25** Quest Points to chop.<br>
- Refer to [Questing](https://www.oldschool.gg/oldschoolbot/minions?Questing) on how to earn Quest Points.

Click [here](https://i.imgur.com/fVG81BQ.png) for **Woodcutting** XP rates.

## Firemaking

You can train Firemaking using `+light [quantity] <logs>`, for example `+light 50 willow`.

### Logs

| **Log**     | **Required level** |
| ----------- | :----------------: |
| Tree        |         1          |
| Achey       |         1          |
| Oak         |         15         |
| Willow      |         30         |
| Teak        |         35         |
| Arctic pine |         42         |
| Maple       |         45         |
| Mahogany    |         50         |
| Yew         |         60         |
| Magic       |         75         |
| Redwood     |         90         |

Click [here](https://i.imgur.com/80iIwN9.png) for **Firemaking** XP rates.

You can now also train Firemaking via the Wintertodt minigame using the `+wt` or `+wintertodt` commands. Fighting the Wintertodt provides item rewards scales to your Woodcutting, Mining, Fishing, Farming, Crafting, and Herblore levels, and xp scaled to your Firemaking level. You need level 50 Firemaking to challenge the Wintertodt, and each attempt requires food to heal yourself from the Wintertodt's attacks, currently a fish which heals >10hp. The speed at which you challenge the Wintertodt increases with a higher Woodcutting level, and the food required is reduced for every piece of the pyromancer outfit you have equipped in your skilling setup, as well as the warm gloves and the fire cape.

## Runecrafting

You can train Runecrafting using `+rc [quantity] <rune>`, for example `+rc 50 law`.

You can boost Runecrafting xp rates by using rune pouches to increase the number of pure essence you can bring per trip to the altar you are using.

### Runes

| **Rune** | **Required level** |
| -------- | :----------------: |
| Air      |         1          |
| Mind     |         2          |
| Water    |         5          |
| Earth    |         9          |
| Fire     |         14         |
| Cosmic   |         27         |
| Chaos    |         35         |
| Astral   |         40         |
| Nature   |         44         |
| Law      |         54         |
| Death    |         65         |
| Wrath    |         95         |

Click [here](https://i.imgur.com/FMxtMSj.png) for **Runecrafting** XP rates.

## Cooking

You can train Cooking using `+cook [quantity] <food>`, for example `+cook 50 bass`.

You can boost Cooking xp rates when attempting to cook fish while having the cooking guantlets equipped which decrease your faliure rate when cooking fish.

### Food

| **Food**    | **Required level** |
| ----------- | :----------------: |
| Beef        |         1          |
| Shrimps     |         1          |
| Chicken     |         1          |
| Anchovies   |         1          |
| Sardine     |         1          |
| Herring     |         5          |
| Mackerel    |         10         |
| Trout       |         15         |
| Cod         |         18         |
| Pike        |         20         |
| Salmon      |         25         |
| Tuna        |         30         |
| Karambwan   |         30         |
| Jug of wine |         35         |
| Lobster     |         40         |
| Bass        |         43         |
| Swordfish   |         45         |
| Monkfish    |         62         |
| Shark       |         80         |
| Anglerfish  |         84         |
| Dark Crab   |         90         |
| Manta Ray   |         91         |

Click [here](https://i.imgur.com/iJuoDbb.png) for **Cooking** XP rates.

## Crafting

You can train Crafting with the `+craft` command. For example, `+craft 100 leather gloves`. To start training Crafting, you will probably want to first kill cows for cowhide, then turn the cowhide into leather using `+craft leather`, then craft leather gloves from those. Alternatively, you can also buy these items from our grand-exchange channel.

To see all the items you can craft, check the [Crafting Wiki Page](https://oldschool.runescape.wiki/w/Crafting) - most of the items are in the bot, with the exact same level and item requirements.

## Prayer

You can train Prayer by burying bones, or offering them to the Chaos altar. For example to bury 100 Dragon bones, you can do `+bury 100 Dragon bones`, or to bury the maximum amount you can: `+bury Dragon bones`. Offering the bones to the Chaos altar works exactly the same, except you use `+offer` instead, for example: `+offer 100 Dragon bones`.

The Chaos Altar works like ingame, your minion will do 1 inventory trips back and forth to sacrifice, with a 10% chance of being PKed in the trip and losing some amount of your inventory of bones (depending on if you got PKed at the start/middle/finish).

The Prayer skill is also required for creating Spirit shields.

## Fletching

You can train fletching with the `+fletch` command. For example, `+fletch 10000 adamant dart`. To start off training fletching, you will want to `+chop` some logs for arrow shafts, and then `+fletch arrow shaft` them into arrow shafts. Alternativley, you can buy logs or unfinished fletching supplies from our #grand-exchange channel in the support server.

To see all the items you can fletch, check out the [Fletching Wiki Page](https://oldschool.runescape.wiki/w/Fletching) - most of the items found there are fletchable in the bot, having the exact same level and item requirements.

You can view your minions' stats using `+m stats`.

### Miscellaneous

- [Questing](https://www.oldschool.gg/oldschoolbot/minions?Questing)
- [Skillcapes](https://www.oldschool.gg/oldschoolbot/minions?Skillcapes)
- [Boosts](https://www.oldschool.gg/oldschoolbot/minions?Boosts)
- [Buyable Items](https://www.oldschool.gg/oldschoolbot/minions?Buyable%20Items)
- [Creatable Items](https://www.oldschool.gg/oldschoolbot/minions?Creatable%20Items)
- [Boss/Monster Requirements](https://www.oldschool.gg/oldschoolbot/minions?Boss%20and%20Monster%20Requirements)
- [Bank Backgrounds](https://www.oldschool.gg/oldschoolbot/minions?Bank%20Backgrounds)
- [Minion Icons](https://www.oldschool.gg/oldschoolbot/minions?Minion%20Icons)
- [Patreon](https://www.oldschool.gg/oldschoolbot/minions?Patreon)

### Bossing

Currently available bosses to kill are:

| ![https://i.imgur.com/jLyLLND.png](https://i.imgur.com/jLyLLND.png) |       Barrows       |
| :-----------------------------------------------------------------: | :-----------------: |
| ![https://i.imgur.com/sKTt3sl.png](https://i.imgur.com/sKTt3sl.png) |      Callisto       |
| ![https://i.imgur.com/GvC5Tco.png](https://i.imgur.com/GvC5Tco.png) |      Cerberus       |
| ![https://i.imgur.com/HdeDjCF.png](https://i.imgur.com/HdeDjCF.png) |   Chaos Elemental   |
| ![https://i.imgur.com/tN9bUAh.png](https://i.imgur.com/tN9bUAh.png) |    Chaos Fanatic    |
| ![https://i.imgur.com/mLeZynK.png](https://i.imgur.com/mLeZynK.png) |  Commander Zilyana  |
| ![https://i.imgur.com/hZUNtgK.png](https://i.imgur.com/hZUNtgK.png) |   Corporeal Beast   |
| ![https://i.imgur.com/eqvQC4C.png](https://i.imgur.com/eqvQC4C.png) | Crazy Archaeologist |
| ![https://i.imgur.com/JfpXrXW.png](https://i.imgur.com/JfpXrXW.png) |   Dagannoth Prime   |
| ![https://i.imgur.com/pO822rj.png](https://i.imgur.com/pO822rj.png) |    Dagannoth Rex    |
| ![https://i.imgur.com/FKVIKMX.png](https://i.imgur.com/FKVIKMX.png) |  Dagannoth Supreme  |
| ![https://i.imgur.com/sLdtsrg.png](https://i.imgur.com/sLdtsrg.png) |  General Graardor   |
| ![https://i.imgur.com/igxsuRU.png](https://i.imgur.com/igxsuRU.png) |     Giant Mole      |
| ![https://i.imgur.com/gVIOuaQ.png](https://i.imgur.com/gVIOuaQ.png) |  K'ril Tsutsaroth   |
| ![https://i.imgur.com/rvqU0Z3.gif](https://i.imgur.com/rvqU0Z3.gif) |   Kalphite Queen    |
| ![https://i.imgur.com/pQFbspB.png](https://i.imgur.com/pQFbspB.png) |  King Black Dragon  |
| ![https://i.imgur.com/OfsrIfN.png](https://i.imgur.com/OfsrIfN.png) |      Kree'arra      |
| ![https://i.imgur.com/Hv6IcBx.gif](https://i.imgur.com/Hv6IcBx.gif) |  Lizardman Shaman   |
| ![https://i.imgur.com/iwGwt1F.png](https://i.imgur.com/iwGwt1F.png) |       Scorpia       |
| ![https://i.imgur.com/HHEZj9X.png](https://i.imgur.com/HHEZj9X.png) |      Venenatis      |
| ![https://i.imgur.com/iSWr25X.gif](https://i.imgur.com/iSWr25X.gif) |       Vet'ion       |
| ![https://i.imgur.com/w9PrhyH.png](https://i.imgur.com/w9PrhyH.png) |       Vorkath       |
| ![https://i.imgur.com/p6d3Wna.gif](https://i.imgur.com/p6d3Wna.gif) |       Zulrah        |

Some bosses have requirements, like Quest points or gear, refer to [Boss and monster requirements](https://www.oldschool.gg/oldschoolbot/minions?Boss%20and%20monster%20requirements) for more information or use the `+monster` command in the bot.

Don't know what you want to kill? Use the `+m k random` command to send your minion off to kill a random monster, limited to monsters you have the requirements to kill.

You can view your minions' killcounts using `+m kc`.

#### Group Bossing

Some bosses are able to be killed in groups, these bosses currently are: All four GWD bosses, and Corp - more bosses are planned to be added. To do group bossing, you create a party, there are two kinds of parties: invite-only and mass. Invite only parties are for you to invite select people on your trip and mass parties can be joined by anyone. Parties have a leader, who is the person who created the party (ran the command).

Note that, similar to ingame, even if you have a very big group of people in a party killing a boss, you're still limited by that bosses respawn time, although the kills can get very very fast if you have lots of people.

Loot is rolled out completely randomly, for example if your party is doing 5 kills, it will give each kill loot to a random party member, the same person can be given loot multiple times, or none at all if unlucky.

Currently, boosts do not apply to group boss trips, however this will be added in the future.

You **cannot** join parties if: you're an ironman or if your minion is busy.

##### Invite-only group bossing

Example of invite-only group bossing party: `+groupkill party corp @Magnaboy @Alexsuperfly @Crow653` - this would make an invite-only party, that only those 3 people can join. Note that, the leader (the person who is running the command) doesn't have to add themselves to the list, they're always included automatically.

After, each user will have to confirm they want to join by clicking on the "join" reaction. The trip will start when all users have confirmed, or if the party leader has clicked the "start" reaction to start early.

##### Mass bossing

Example of a mass bossing party: `+groupkill mass corp` - this would make a mass party, that ANYONE can join. The trip will start after 2 minutes automatically, or when the party leader clicks the "start" reaction.

#### Fight Caves

You can now challenge the Fight Caves and TzTok-Jad to recieve a fire cape, tokkul, and the TzRek-Jad pet using the `+fightcaves` command. Requirements: total +160 range bonus equipped to your range gear setup, 43 prayer, 10x Prayer Potion (4), 4x Super Restore (4), and 6x Saradomin Brew (4) per attempt, some of which may be returned to you should you fail before the final wave. You can make the 4 dose potions from 3, 2, and 1 dose drops using the `+decant` command. Better range gear will reduce the time each attempt takes, as will total Jad kc. Having a Saradomin Godsword equipped in your melee gear setup will reduce your chances of dying before Jad by 4%, and the number of total attempts you have made will determine your chances of killing Jad when he is reached.

If you have extra fire capes, you can gamble them for an additional roll at the TzRek-Jad pet using the `+capegamble` command.

#### Equipping Gear

When sending your minion out on boss or skilling trips, you can equip it with gear to improve its speed and effeciency. For convenience, there is a gear setup for melee, range, mage, skilling, and misc. Depending on the activity your minion is doing will depend on which gear is used. For example, taking on the fightcaves uses your minion's **range** gear setup as well as the Saradomin Godsword if it is equipped in your **melee** gear setup. Whereas going mining will use your minion's **skilling** gear setup. You can equip any equippable items you want into the different setups.
When an item is equipped, it is removed from your bank to the gear setup. When unequipped, the item moves back to your bank.

To **equip** an item into a setup, use: `+equip [setup] [item]`. For example, to equip a Bandos chestplate to the melee setup, you would use the command: `+equip melee bandos chestplate`. To **unequip** an item from a setup, use: `+unequip [setup] [item]`. For example: `+unequip melee bandos chestplate`.

To view your currently equipped gear, use: `+gear [setup]`. For example, to see your skilling setup, use: `+gear skilling`.

Just like dropping a pet ingame and having it follow you, your minion can also equip a pet. This will keep your minion company while it's out working hard to earn you items and gp. To equip a pet, use: `+equippet [pet name]` and it will show on all your gear setups. To unequip it, use: `+unequippet`.

## Questing

Questing in the bot is simple and easy, and roughly 20% faster than ingame. Instead of doing specific quests, you just "quest" and gain QP for "questing". You can keep questing until you reach the max QP. The amount of QP you recieve per trip scales down as you progress, with averages of 4 QP/hr from 0 to 100 QP, 3 QP/hr from 100-200 QP, and 2 QP/hr from 200-275 QP.

Quest points are required to kill some bosses (e.g. Vorkath) and required to buy some items (e.g. Barrows gloves).

Questing recieves a 10% boost if you have the full Graceful outfit equipped in your skilling gear setup.

## Skillcapes

Upon reaching level 99 in a skill, you can purchase a skillcape for 99k by typing `+skillcape <skill_name>`. If it's your first 99, you'll get an untrimmed cape.

# Boss and Monster Requirements

| **Boss**          | **QP required** |                                                               **Gear required**                                                               | **Skill(s) required** |
| ----------------- | :-------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------: |
| Barrows           |       N/A       |                                                                      N/A                                                                      |       43 Prayer       |
| Lizardman shaman  |       30        |                                                                Karils Crossbow                                                                |       43 Prayer       |
| Zulrah            |       75        |                                Armadyl chestplate, Armadyl chainskirt, Ahrim's robetop, and Ahrim's robeskirt                                 |       43 Prayer       |
| Vorkath           |       205       |                                                    Armadyl chestplate, Armadyl chainskirt                                                     |       43 Prayer       |
| Giant Mole        |       N/A       |                                                               Full Dharok's set                                                               |       43 Prayer       |
| Callisto          |       N/A       |                                                               Full Verac's set                                                                |          N/A          |
| Venenatis         |       N/A       |                                                               Full Verac's set                                                                |          N/A          |
| King Black Dragon |       N/A       |                                                              Anti-Dragon shield                                                               |          N/A          |
| Chaos Elemental   |       N/A       |                            Karil's leathertop or Black d'hide body and Karil's leatherskirt or Black d'hide chaps                             |          N/A          |
| Corporeal Beast   |       N/A       |                                                               Zamorakian spear                                                                |       43 Prayer       |
| Cerberus          |       N/A       | Bandos chestplate or Torag's platebody or Dharok's platebody, Bandos tassets or Torag's platelegs or Dharok's platelegs, and Zamorakian spear |       43 Prayer       |
| Commander Zilyana |       75        |                            Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                            | 43 Prayer, 70 Agility |
| General Graardor  |       75        |                                                                      N/A                                                                      |       43 Prayer       |
| Kree'Arra         |       75        |                            Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                            |       43 Prayer       |
| K'ril Tsutsaroth  |       75        |                            Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                            |       43 Prayer       |
| Kalphite Queen    |       N/A       |                                 Verac's flail, Karil's leathertop or Black d'hide top, and Verac's plateskirt                                 |       43 Prayer       |
| Dagannoth Prime   |       N/A       |                    Full Guthan's, Armadyl chestplate or Karil's leathertop and Armadyl chainskirt or Karil's leatherskirt                     |       43 Prayer       |
| Dagannoth Rex     |       N/A       |                        Full Guthan's, Bandos chestplate or Torag's chestplate, and Bandos tassets or Torag's platelegs                        |       43 Prayer       |
| Dagannoth Supreme |       N/A       |                        Full Guthan's, Bandos chestplate or Torag's chestplate, and Bandos tassets or Torag's platelegs                        |       43 Prayer       |

# Buyable Items

You can purchase these items by typing `+buy <item>`. Some require QP, and have higher costs than ingame.

| **Item**                                      | **Quest points required** | **Price** |
| --------------------------------------------- | :-----------------------: | :-------: |
| Quest Point Cape                              |            275            |    99k    |
| Helm of Neitiznot                             |            75             |   500k    |
| Iban's Staff                                  |            30             |   250k    |
| Barrelchest Anchor                            |            30             |    2m     |
| Magic Secateurs                               |            40             |   2.5m    |
| Goldsmith gauntlets                           |            25             |    1m     |
| Cooking gauntlets                             |            25             |    1m     |
| Anti-dragon shield                            |            35             |    10k    |
| Barrows gloves                                |            175            |    1m     |
| Dragon gloves                                 |            107            |   850k    |
| Rune gloves                                   |            85             |   700k    |
| Adamant gloves                                |            65             |   600k    |
| Mithril gloves                                |            50             |   500k    |
| Black gloves                                  |            35             |   400k    |
| Steel gloves                                  |            25             |   300k    |
| Iron gloves                                   |            20             |   200k    |
| Bronze gloves                                 |            10             |   100k    |
| Hardleather gloves                            |             5             |    50k    |
| Huge Fishing Bait Pack (10,000x Fishing Bait) |            N/A            |    50k    |
| Feather Pack (1,000x Feathers)                |            N/A            |    10k    |
| Huge Jug Pack (300x Jugs of water)            |            N/A            |    30k    |

# Creatable Items

These items can be made by using the `+create <item>` command.

| **Item**               |                       **Input item(s) required**                       |  **Stat(s) required**  |
| ---------------------- | :--------------------------------------------------------------------: | :--------------------: |
| Godsword Blade         |                        Godsword Shard 1, 2 & 3                         |      80 Smithing       |
| Godsword               |                          Godsword Blade, Hilt                          |      80 Smithing       |
| Dragonfire Shield      |                  Anti-dragon Shield, Draconic Visage                   |      90 Smithing       |
| Dragonfire Ward        |                  Anti-dragon Shield, Skeletal Visage                   |      90 Smithing       |
| Infernal Pickaxe       |                   Dragon Pickaxe, Smouldering Stone                    |      85 Smithing       |
| Infernal Axe           |                     Dragon Axe, Smouldering Stone                      |     85 Firemaking      |
| Odium Ward             |                         Odium Shard 1, 2, & 3                          |          None          |
| Malediction Ward       |                       Malediction Shard 1, 2 & 3                       |          None          |
| Blessed Spirit Shield  |                       Spirit Shield, Holy Elixir                       |       85 Prayer        |
| Spectral Spirit Shield |                 Blessed Spirit Shield, Spectral Sigil                  | 90 Prayer, 85 Smithing |
| Arcane Spirit Shield   |                  Blessed Spirit Shield, Arcane Sigil                   | 90 Prayer, 85 Smithing |
| Elysian Spirit Shield  |                  Blessed Spirit Shield, Elysian Sigil                  | 90 Prayer, 85 Smithing |
| Master Clue            |                Clue Scroll Easy, Medium, Hard, & Elite                 |          None          |
| Holy Book              |                      Saradomin Page 1, 2, 3, & 4                       |    35 Agility, 5 QP    |
| Book of Balance        |                        Guthix Page 1, 2, 3, & 4                        |    35 Agility, 5 QP    |
| Unholy Book            |                       Zamorak Page 1, 2, 3, & 4                        |    35 Agility, 5 QP    |
| Book of Law            |                       Armadyl Page 1, 2, 3, & 4                        |    35 Agility, 5 QP    |
| Book of War            |                        Bandos Page 1, 2, 3, & 4                        |    35 Agility, 5 QP    |
| Book of Darkness       |                       Ancient Page 1, 2, 3, & 4                        |    35 Agility, 5 QP    |
| Ava's Accumulator      |                            75x Steel Arrows                            |         30 QP          |
| Ava's Assembler        |         75x Mithril Arrows, Ava's Accumulator, Vorkath's Head          |         205 QP         |
| Prospector Helmet      |                           40x Golden Nuggets                           |          None          |
| Prospector Jacket      |                           60x Golden Nuggets                           |          None          |
| Prospector Legs        |                           50x Golden Nuggets                           |          None          |
| Prospector Boots       |                           30x Golden Nuggets                           |          None          |
| Mining Gloves          |                       60x Unidentified Minerals                        |          None          |
| Superior Mining Gloves |                       120x Unidentified Minerals                       |          None          |
| Expert Mining Gloves   | 60x Unidentified Minerals, 1x Mining Gloves, 1x Superior Mining Gloves |          None          |
| Small Pouch            |                              10x Leather                               |          None          |
| Medium Pouch           |                              20x Leather                               |      10 Crafting       |
| Large Pouch            |                              30x Leather                               |      20 Crafting       |
| Giant Pouch            |                              40x Leather                               |      30 Crafting       |

# Bank Backgrounds

If you meet the requirements and costs of a background, you can get it using `+bankbg <name>`. The image will replace the background of your bank. Bank backgrounds require that you pay GP, items and having certain items in your collection log, they are quite hard to obtain.

Click on the bank bg name to see what it looks like.

| **Name**                                                                                                           | **GP Cost** |                  **Item Cost**                   |                                 **Collection Log Items Needed**                                 |
| ------------------------------------------------------------------------------------------------------------------ | :---------: | :----------------------------------------------: | :---------------------------------------------------------------------------------------------: |
| [Default](https://github.com/gc/oldschoolbot/blob/master/resources/images/bank_backgrounds/1.jpg?raw=true)         |      0      |                                                  |                                                                                                 |
| [Bandos](https://github.com/gc/oldschoolbot/blob/master/resources/images/bank_backgrounds/7.jpg?raw=true)          |    100m     |                 The 4 Godswords                  |                                  Entire GWD log including pets                                  |
| [Corporeal Beast](https://github.com/gc/oldschoolbot/blob/master/resources/images/bank_backgrounds/8.jpg?raw=true) |    100m     | 1 spectral spirit shield, 1 arcane spirit shield | Entire Corporeal Beast log including pet (4x spirit shield, 4x holy elixir for all the shields) |
| [Casket (Legend Arts)](https://github.com/gc/oldschoolbot/blob/master/resources/images/bank_backgrounds/9.jpg)     |    100m     |                                                  |                                The 4 clue milestone item rewards                                |

# Minion Icons

You can sacrifice items, and their GP value will go towards you unlocking new minion icons. You will automatically receive the icon immediately after sacrificing enough GP. You can see a leaderboard of who has sacrificed the most using `+lb sacrifice`.

You can sacrifice items using `+sacrifice [quantity] <item>`, like `+sacrifice Bandos chestplate` or `+sacrifice 1000 gold ore`. You cannot sacrifice GP, instead you should buy items off other players with your GP and sacrifice those.

|                               Icon                                | Amount Required |
| :---------------------------------------------------------------: | :-------------: |
| ![](https://cdn.discordapp.com/emojis/679007949108281357.png?v=1) |        0        |
| ![](https://cdn.discordapp.com/emojis/673561629115416616.png?v=1) |      100m       |
| ![](https://cdn.discordapp.com/emojis/673561610366746635.png?v=1) |      500m       |
| ![](https://cdn.discordapp.com/emojis/673561610228465664.png?v=1) |       1b        |
| ![](https://cdn.discordapp.com/emojis/673561609834070047.png?v=1) |       5b        |
| ![](https://cdn.discordapp.com/emojis/673561609913892899.png?v=1) |       10b       |

# Patreon

The Patreon is a way for users to donate to me (Magnaboy), if you wish. It's entirely your choice, if you want to. I will never sell items/GP from the bot for money, nor P2W perks/advantages.

You can donate to me on Patreon here: [https://www.patreon.com/oldschoolbot](https://www.patreon.com/oldschoolbot)

You can also read the [FAQ](https://www.oldschool.gg/oldschoolbot/faq) for answers to common questions.
