# Cossacks AI Documentation

This document is a work in progress of all the details that I've been able to understand by trying and testing each part of the code. I'll keep updating this document as and when I make progress. If possible, will also put the source code here at a later point. I'm not sure if it's legal yet, depends on what GSC Gameworld allows (following on the pattern of everything else, there's not really much information about it!).

I can be reached at plasty.grove@SomeEmailCompany (Hint: Very popular email by very popular search engine whose name starts with G) :)

# Installation

Follow these steps to get a working environment:

1.  Install Visual Studio 6 (Um ... er ... ah, where can I get this? \<koff\>\<koff\>torr****\<koff\>\<koff\>)
2.	Use the workspace (dsw) file in 112_C_I_BTW_AI_Sour\Cossacks_I_BTW_AI_Source\AI_0995\AI
3.	To build for all countries, run build batch and check the ‘Release’ versions for all countries
4.	Most of the countries have all header files in ‘External Dependencies’. Some have it in ‘Header files’
5.	All countries are linked to the same Dependencies i.e. changing the AI of one will change it for all countries
6.	Execution starts in Scripts.h in the function MainScript()
7.	In the Switch statement, add Dummy() under case LT_LAND and add break. Create empty function void Dummy(void) in Extraction.h. When you play the game, you will see that the units aren’t doing anything

# Functions Documentation

These are the various functions in the code. At a later point, maybe I'll seperate them file-wise, but too difficult to do it right now.

1.	TryUnit(GAMEOBJ* UnitType,int Max,byte CostPercent,byte Probability) – Try to create/build a unit/building depending on the constraints available
    1. UnitType – The type of unit i.e. Peasant, Infantry etc
    2. Max – Maximum number of that particular unit allowed
    3. CostPercent – Create unit only if the the cost of creating the resource is this much percentage of the total. Otherwise don’t create
    4. Probability – Not sure, just use 100%
2.	void SetPDistribution(int OnFood,int OnWood,int OnStone) – How to distribute them on food, wood and stone. Doesn’t seem to be working properly, need a bit more testing

# Nomenclature

What the various units are in __Plain English__:

MELN – Mill  
SKLAD – Storehouse  
KAZ17 – 17th Century Barracks  
KUZNICA – Blacksmith  
RINOK – Market  
INFANTRY – Pikemen, Officers, Drummers automatically created and start attacking  
DIPCENTER – Diplomatic Center  
OFFICER – 17C Barracks officer  
STREL17 – 17C Musketeer  
PUSHKA17 – Illegal Unit (Causes game to crash)  
MORTIRA17 – Illegal Unit (Causes game to crash)  
