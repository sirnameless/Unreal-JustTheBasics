# Unreal-JustTheBasics
Unreal Engine 4 - Just the Basics. A very basic skeleton with helpful examples to build any game project from

## Intro

This is an Unreal project utilizing Blueprints to create a game with a main menu, basic gameplay map, and a game over screen. Supports 1 to 2 players.

2D assets are from David Hellman who supplies assets for free from the incredible and unforgettable gaming experience "Braid," available here: http://www.davidhellman.net/braidbrief.htm

## Create a UI

We'll start by designing the user interface in a blank Main Menu map. Click "Add New" in the Content Browser, go to User Interface, then create a new Widget Blueprint. Drag a Text object over for the title, 2 buttons, and then two more text objects to place on top of the button objects. In the Details view, select Anchors, hold Shift, and click on an Anchor selection to easily center your objects. Adjust using the X/Y values in the Details view. Change the text objects placed on each button to something like "Play 1 Player Game" and "Play 2 Player Game."

![Create a UI](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/ui_setup.png)

Close the widget editor, then click on "Blueprints," and open the Level blueprint. From "Event BeginPlay," drag from the white Execute marker and add a "Create Main Menu Blueprint Widget." This creates the widget in the scene, but you won't actually be able to see it unless you add it to the viewport using the "Add to Viewport" event, and connect the exec and value connectors.

![Add UI to Viewport](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/add_to_viewport.png)

## Create Global Variables / Instances

To pass variables from one map to the next, we can use a custom global instance. Click "Add New" in your Content Browser, then select "Blueprint Class." Use the search bar to search for "Game Instance." Select the game instance and create a new global instance.

![Create a Game Instance](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/new_bp_game_instance_parent.png)

Click the plus/add button on "Variables" to create a "Players" variable. Move over to the Details view - change the Players variable's type from Boolean to Integer. We'll use this variable to track how many players we want the game to start with, dependant on user selection on the main menu.

![Create a Game Instance Variable](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/game_instance_variable.png)

## Create UI Logic

Yay! We're programming using blueprints! Go back to your Main Menu widget and select either button that you created. In the Details view, scroll down to "Events." Click on the plus/add button for an OnClicked event. Following the logic pictured below, we will SET the Players variable of our custom global instance to 1 or 2, depending on which button the user pressed, then we'll open our gameplay level.

![Create a Main Menu Blueprint](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/main_menu_bp.png)

## Setup Basic Gameplay & Logic to Determine Number of Players

![Import a FBX file](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/import_fbx_into_level.png)

![Actor Tags](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/actor_tags.png)

![Open Character Blueprint](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/open_character_bp.png)

![Create Player Logic](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/players_logic.png)

## Let us go back to gameplay from a Game Over Screen

![Create a Game Over Blueprint](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/game_over_menu_bp.png)

## Create 2D Decals and Animations

![Create a transparent decal](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/transparent_decal.png)

![Create Decal Blueprints](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/decal_bp.png)

![Extract Sprite Sheet](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/sprite_sheet_extract.png)

![Create Flipbook](https://raw.githubusercontent.com/sirnameless/Unreal-JustTheBasics/master/readmefiles/create_flipbook.png)
