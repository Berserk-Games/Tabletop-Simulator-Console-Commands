# Console Commands



## `action_cut`

Cut specified component at specified point.

USAGE: `action_cut [-p &lt;point>|-c <count>] [<guid>...]`

Cut deck/stack in half. Cut point &lt;defaults to splitting in half, or use one of:

-p = between 0.0 and 1.0, a ratio over container size.

-c = count of items.


## `action_deal`

Deal from specified component.

USAGE: `action_deal [-c <count>] <guid> [<player>...]`

Deal <count> cards (default 1) from component specified by <guid> to each <player>. If no <player> provided then deal to each seated player.


## `action_draw`

Draw from specified component.

USAGE: `action_draw [-c <count>] [<guid>...]`

Draw from component specified by <guid>. If no <guid> provided then the mouse/selection will be used.

 -c = specify number of cards to draw


## `action_flip`

Flip specified component.

USAGE: `action_flip [<guid>...]`

Flip component specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `action_group`

Group specified components.

USAGE: `action_group [<guid>...]`

Group components specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `action_layout`

Layout specified component.

USAGE: `action_layout [<guid>...]`

Layout component specified by <guid> if its in (or is) a valid Layout Zone. If no <guid> provided then the mouse/selection will be used.


## `action_lock`

Lock specified component.

USAGE: `action_lock [<guid>...]`

Lock/unlock component specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `action_popout`

Pop-out to screen specified component.

USAGE: `action_popout [<guid>...]`

Pop-out to screen component specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `action_randomize`

Randomize (shuffle/roll/etc.) specified component.

USAGE: `action_randomize [<guid>...]`

Randomize component specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `action_rotate`

Rotate specified component.

USAGE: `action_rotate > [-z] <angle> [<guid>...]`

Rotate component specified by <guid>. <angle> is a multiple of 15.

If no <guid> provided then the mouse/selection will be used.

 -z = rotate around z axis instead.


## `action_search`

Search specified component.

USAGE: `action_search [-s <search text>] [-c <count>] [<guid>]`

Search component specified by <guid>. If no <guid> provided then the mouse/selection will be used.

 -s <text> = specific search text

 -c <count> = max cards when searching deck


## `action_split`

Split specified component into piles.

USAGE: `action_split <piles> [<guid>...]`

Split container specified by <guid> into <piles>.


## `action_spread`

Spread specified deck component face-up across table.

USAGE: `action_spread [-d <distance>] [<guid>]`

Split container specified by <guid> into <piles>.


## `action_state_next`

Increment state of specified component.

USAGE: `action_state_next [<guid>]`

Increment state of component specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `action_state_prev`

Decrement state of specified component.

USAGE: `action_state_prev [<guid>]`

Decrement state of component specified by <guid>. If no <guid> provided then the mouse/selection will be used.


## `add`

Add a value to a numerical variable.

USAGE: `add <variable> <value> [<modulus>]`

Sets <variable> to its current value + <value>, modulo the optional parameter if present.


## `alias`

Creates an alias for another command using specified parameters as defaults.

USAGE: `alias <label> <command> [<parameters] OR alias <label> -d OR alias <new_prefix>* <old_prefix>*`

Creates an alternate way to call <command>.  If <parameters> are provided they will automatically be applied when using that alias.

Use * create an alias for all commands with specified prefix.

-d = deletes an already existing alias.



If <label> is a toggle variable you may prefix with + or - to attach <command> to it; when it changes to that value the command will execute.


## `append`

Add text to a text variable.

USAGE: `append [-n] <variable> [<text>]`

Appends <text> to <variable>.  If no <text> specified then appends last entered command (before this one).

-n = do not insert newline before appending.


## `autoexec`

Batch which automatically runs every time the game restarts.

USAGE: `autoexec [value] OR autoexec -e`

Displays value of `autoexec`.  If value parameter provided then sets `autoexec` to value specified.

   -e = Edit in UI editor


## `autosave_interval`

Time in seconds between each auto save. If set to 0 then auto save is disabled.

USAGE: `autosave_interval [value]`

Displays value of `autosave_interval`.  If value parameter provided then sets `autosave_interval` to value specified.




## `autosave_log`

If ON then when an auto save happens it will be logged in the system console.

USAGE: `autosave_log [ON|OFF|TOGGLE]`

Displays value of `autosave_log`.  If value parameter provided then sets `autosave_log` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!autosave_log` = '`autosave_log TOGGLE`'


## `autosave_slots`

The number of auto save slots. If set to 0 then auto save is disabled.

USAGE: `autosave_slots [value]`

Displays value of `autosave_slots`.  If value parameter provided then sets `autosave_slots` to value specified.




## `bind`

Bind a command to a key.

USAGE: `bind [[+|-|!]<key> [<command>]]`

If <command> is specified then it is bound to trigger whenever <key> is pressed.

Optional prefixes on <key>:

   + = trigger on key press (same as no prefix)

   - = trigger on key release

   ! = trigger on key long press

If no <command> specified will display whatever <key> is currently bound to, or all bindings if no <key> specified.


## `bool`

Creates a variable which can be ON or OFF.

USAGE: `store_toggle <variable> [<value>]`

Creates a variable which can be ON or OFF.  It will be set to <value> if it is provided, else OFF.


## `bootexec`

Batch which automatically runs when the game first starts up.

USAGE: `bootexec [value] OR bootexec -e`

Displays value of `bootexec`.  If value parameter provided then sets `bootexec` to value specified.

   -e = Edit in UI editor


## `broadcast`

Broadcast text.

USAGE: `broadcast <text>`

Broadcasts the specified <text>.


## `camera_clear_saved_positions`

Resets camera saved positions.

USAGE: `camera_clear_saved_positions`


## `camera_load`

Set camera position to saved position.

USAGE: `camera_load [value]`

Displays value of `camera_load`.  If value parameter provided then sets `camera_load` to value specified.




## `camera_load_zero`

Set camera position to saved position.  Position is zero-indexed (so one less than displayed in UI)

USAGE: `camera_load_zero [value]`

Displays value of `camera_load_zero`.  If value parameter provided then sets `camera_load_zero` to value specified.




## `camera_reset_on_load`

When ON the camera will reset its position when you load a game.

USAGE: `camera_reset_on_load [ON|OFF|TOGGLE]`

Displays value of `camera_reset_on_load`.  If value parameter provided then sets `camera_reset_on_load` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!camera_reset_on_load` = '`camera_reset_on_load TOGGLE`'


## `camera_restore_saved_positions`

Restore camera saved positions.

USAGE: `camera_restore_saved_positions [<label>]`

Restore camera saved positions.  Read from default store, or <label> if specified.


## `camera_rotation_rate`

Sets how fast the camera rotates to the saved direction.

USAGE: `camera_rotation_rate [value]`

Displays value of `camera_rotation_rate`.  If value parameter provided then sets `camera_rotation_rate` to value specified.




## `camera_save`

Save camera position.

USAGE: `camera_save [value]`

Displays value of `camera_save`.  If value parameter provided then sets `camera_save` to value specified.




## `camera_save_zero`

Save camera position.  Position is zero-indexed (so one less than displayed in UI)

USAGE: `camera_save_zero [value]`

Displays value of `camera_save_zero`.  If value parameter provided then sets `camera_save_zero` to value specified.




## `camera_store_saved_positions`

Store camera saved positions.

USAGE: `camera_store_saved_positions [<label>]`

Store camera saved positions.  Stores as default, or as <label> if specified.  If no saved cameras exist then <label> will be removed.


## `card_is_a_deck_for_hotkeys`

When ON pressing a number on a card will draw it.  When OFF card will be treated like any other component (changing rotation value / state / etc.).

USAGE: `card_is_a_deck_for_hotkeys [ON|OFF|TOGGLE]`

Displays value of `card_is_a_deck_for_hotkeys`.  If value parameter provided then sets `card_is_a_deck_for_hotkeys` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!card_is_a_deck_for_hotkeys` = '`card_is_a_deck_for_hotkeys TOGGLE`'


## `chat_copy`

Copy text from current chat window to clipboard.

USAGE: `chat_copy`


## `chat_filter`

When ON chat messages will be filtered.

USAGE: `chat_filter [ON|OFF|TOGGLE]`

Displays value of `chat_filter`.  If value parameter provided then sets `chat_filter` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!chat_filter` = '`chat_filter TOGGLE`'


## `chat_font_size`

Sets size of chat font.

USAGE: `chat_font_size [value]`

Displays value of `chat_font_size`.  If value parameter provided then sets `chat_font_size` to value specified.




## `chat_input`

Activate chat input.

USAGE: `chat_input`

Activate chat input box.


## `chat_input_clear_on_dismiss`

When ON chat input is cleared when chat is dismissed.

USAGE: `chat_input_clear_on_dismiss [ON|OFF|TOGGLE]`

Displays value of `chat_input_clear_on_dismiss`.  If value parameter provided then sets `chat_input_clear_on_dismiss` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!chat_input_clear_on_dismiss` = '`chat_input_clear_on_dismiss TOGGLE`'


## `chat_refresh_filter`

Refresh the IRC chat filter.

USAGE: `chat_refresh_filter`


## `chat_tab_game`

Switch to GAME tab.

USAGE: `chat_tab_game`

Switch chat tab to GAME tab, if available.


## `chat_tab_global`

Switch to GLOBAL tab.

USAGE: `chat_tab_global`

Switch chat tab to GLOBAL tab, if available.


## `chat_tab_system`

Switch to SYSTEM tab.

USAGE: `chat_tab_system [-f]`

Switch chat tab to SYSTEM tab, if available.

-f = focus input


## `chat_tab_team`

Switch to TEAM tab.

USAGE: `chat_tab_team`

Switch chat tab to TEAM tab, if available.


## `chat_visible`

Whether the chat window is currently visible.

USAGE: `chat_visible [ON|OFF|TOGGLE]`

Displays value of `chat_visible`.  If value parameter provided then sets `chat_visible` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!chat_visible` = '`chat_visible TOGGLE`'


## `choose`

Allow the user to make a choice from a drop-down.

USAGE: `choose <variable> [-t <title>] <option> [<option>...]`

If <variable> is a number, set it to index of selected option.

If <variable> is text, set it to the selected option.


## `clear`

Clears a text variable.

USAGE: `clear <variable>`

Clears specified text variable.


## `color`

Your current player color.  Changing it will change your seat.

USAGE: `color [<color>]`

Returns your current color.  If <color> provided will attempt to swap you to that color.


## `commands`

Lists all commands (not including variables).

USAGE: `commands [-a] [prefix]`

Displays all command roots which are not variables.

If prefix is supplied then only commands which start with it will be displayed.

-a = display all commands, not just command roots.


## `component_default_autoraise`

Default state of component toggle for auto-raise.

USAGE: `component_default_autoraise [ON|OFF|TOGGLE]`

Displays value of `component_default_autoraise`.  If value parameter provided then sets `component_default_autoraise` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_autoraise` = '`component_default_autoraise TOGGLE`'


## `component_default_grid`

Default state of component toggle for grid.

USAGE: `component_default_grid [ON|OFF|TOGGLE]`

Displays value of `component_default_grid`.  If value parameter provided then sets `component_default_grid` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_grid` = '`component_default_grid TOGGLE`'


## `component_default_hands`

Default state of component toggle for hands.

USAGE: `component_default_hands [ON|OFF|TOGGLE]`

Displays value of `component_default_hands`.  If value parameter provided then sets `component_default_hands` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_hands` = '`component_default_hands TOGGLE`'


## `component_default_ignore_fow`

Default state of component toggle for ignore fog-of-war.

USAGE: `component_default_ignore_fow [ON|OFF|TOGGLE]`

Displays value of `component_default_ignore_fow`.  If value parameter provided then sets `component_default_ignore_fow` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_ignore_fow` = '`component_default_ignore_fow TOGGLE`'


## `component_default_reveal_fow`

Default state of component toggle for reveal fog-of-war.

USAGE: `component_default_reveal_fow [ON|OFF|TOGGLE]`

Displays value of `component_default_reveal_fow`.  If value parameter provided then sets `component_default_reveal_fow` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_reveal_fow` = '`component_default_reveal_fow TOGGLE`'


## `component_default_snap`

Default state of component toggle for snap.

USAGE: `component_default_snap [ON|OFF|TOGGLE]`

Displays value of `component_default_snap`.  If value parameter provided then sets `component_default_snap` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_snap` = '`component_default_snap TOGGLE`'


## `component_default_sticky`

Default state of component toggle for sticky.

USAGE: `component_default_sticky [ON|OFF|TOGGLE]`

Displays value of `component_default_sticky`.  If value parameter provided then sets `component_default_sticky` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_sticky` = '`component_default_sticky TOGGLE`'


## `component_default_tooltip`

Default state of component toggle for tooltip.

USAGE: `component_default_tooltip [ON|OFF|TOGGLE]`

Displays value of `component_default_tooltip`.  If value parameter provided then sets `component_default_tooltip` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_default_tooltip` = '`component_default_tooltip TOGGLE`'


## `component_examine`

Currently examined component.

USAGE: `component_examine [<GUID>|<color>]`

If <GUID> specified then start examining that component. If <color> specified then start examining that player's hand zone.


## `component_hiders` (admin)

Displays any hiders attached to component.

USAGE: `component_hiders [<guid>]`

Displays any hiders attached to component specified by <guid>. If no <guid> provided then that last held component will be used.


## `component_locked`

Locked state of specified component.

USAGE: `component_locked <guid> [<locked>]`

Locked state of component specified by <guid>.


## `component_move`

Move a component.

USAGE: `component_move <GUID> [-f] <translation>`

Move specified component.  <translation> is a vector (x,y,z).  Use '-' for any axis to leave it as is.-f = fast


## `component_override_defaults`

When ON components spawned from UI will use defaults set by `component_default_...` commands.

USAGE: `component_override_defaults [ON|OFF|TOGGLE]`

Displays value of `component_override_defaults`.  If value parameter provided then sets `component_override_defaults` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_override_defaults` = '`component_override_defaults TOGGLE`'


## `component_position`

Set position of a component.

USAGE: `component_position <GUID> [-f] <position>`

Move specified component to specified <position>.  <position> is a vector (x,y,z).  Use '-' for any axis to leave it as is.-f = fast


## `component_rotate`

Rotate a component.

USAGE: `component_rotate <GUID> [-f] <rotation>`

Rotate specified component.  <rotation> is a vector (x,y,z).  Use '-' for any axis to leave it as is.-f = fast


## `component_rotation`

Set rotation of a component.

USAGE: `component_rotation <GUID> [-f] <rotation>`

Rotate specified component to specified <rotation>.  <rotation> is a vector (x,y,z).  Use '-' for any axis to leave it as is.-f = fast


## `component_spread_cards_per_row`

maximum number of cards per row when the Spread action is used.

USAGE: `component_spread_cards_per_row [value]`

Displays value of `component_spread_cards_per_row`.  If value parameter provided then sets `component_spread_cards_per_row` to value specified.




## `component_spread_distance`

Distance cards are spread apart when the Spread action is used.

USAGE: `component_spread_distance [value]`

Displays value of `component_spread_distance`.  If value parameter provided then sets `component_spread_distance` to value specified.




## `component_spread_row_distance`

Distance between rows when cards are spread apart when the Spread action is used.

USAGE: `component_spread_row_distance [value]`

Displays value of `component_spread_row_distance`.  If value parameter provided then sets `component_spread_row_distance` to value specified.




## `component_state`

State of specified component.

USAGE: `component_state <guid> [<state>]`

State of component specified by <guid>.


## `component_tooltip_delay`

Length of time you must hover over a game component before the description tooltip is displayed.

USAGE: `component_tooltip_delay [value]`

Displays value of `component_tooltip_delay`.  If value parameter provided then sets `component_tooltip_delay` to value specified.




## `component_update_visibility`

Force component visibility calculation to run.

USAGE: `component_update_visibility [<GUID>]`




## `component_wrap_states`

When ON the Next State and Prev State commands will wrap around available states.

USAGE: `component_wrap_states [ON|OFF|TOGGLE]`

Displays value of `component_wrap_states`.  If value parameter provided then sets `component_wrap_states` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!component_wrap_states` = '`component_wrap_states TOGGLE`'


## `console_hotkey_lock`

When ON disables typing of the System Console keyboard shortcut; it will then *always* toggle the System Console

USAGE: `console_hotkey_lock [ON|OFF|TOGGLE]`

Displays value of `console_hotkey_lock`.  If value parameter provided then sets `console_hotkey_lock` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!console_hotkey_lock` = '`console_hotkey_lock TOGGLE`'


## `debug_external_api`

When ON activates debug logging for extrnal api.

USAGE: `debug_external_api [ON|OFF|TOGGLE]`

Displays value of `debug_external_api`.  If value parameter provided then sets `debug_external_api` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!debug_external_api` = '`debug_external_api TOGGLE`'


## `debug_list_resources`

Lists number of currently loaded resources.

USAGE: `debug_list_resources`


## `deck_can_spread_facedown`

When ON and you use the Spread action on a deck which is face-down, its cards will remain face-down after spreading.

USAGE: `deck_can_spread_facedown [ON|OFF|TOGGLE]`

Displays value of `deck_can_spread_facedown`.  If value parameter provided then sets `deck_can_spread_facedown` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!deck_can_spread_facedown` = '`deck_can_spread_facedown TOGGLE`'


## `default_host_name`

Default server name when hosting.

USAGE: `default_host_name [value] OR default_host_name -e`

Displays value of `default_host_name`.  If value parameter provided then sets `default_host_name` to value specified.

   -e = Edit in UI editor


## `default_host_password`

Default server password when hosting.

USAGE: `default_host_password [value] OR default_host_password -e`

Displays value of `default_host_password`.  If value parameter provided then sets `default_host_password` to value specified.

   -e = Edit in UI editor


## `delete`

Deletes a user-created variable.

USAGE: `delete <variable>`

Deletes a variable.  May only delete variables created with 'store_toggle', 'store_number', and 'store_text'.


## `dev_autoconfirm_browser_url_change`

Browser objects will load all URLs without prompting.  Danger!

USAGE: `dev_autoconfirm_browser_url_change [ON|OFF|TOGGLE]`

Displays value of `dev_autoconfirm_browser_url_change`.  If value parameter provided then sets `dev_autoconfirm_browser_url_change` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!dev_autoconfirm_browser_url_change` = '`dev_autoconfirm_browser_url_change TOGGLE`'


## `dev_highlight_3d` (admin)

Use 3D object highlight system.

USAGE: `dev_highlight_3d [ON|OFF|TOGGLE]`

Displays value of `dev_highlight_3d`.  If value parameter provided then sets `dev_highlight_3d` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!dev_highlight_3d` = '`dev_highlight_3d TOGGLE`'


## `dev_highlight_opacity`

Opacity of highlighter when using 3D highlighting.

USAGE: `dev_highlight_opacity [value]`

Displays value of `dev_highlight_opacity`.  If value parameter provided then sets `dev_highlight_opacity` to value specified.




## `dev_highlight_scalar`

Scale multiplier of highlighter when using 3D highlighting.

USAGE: `dev_highlight_scalar [value]`

Displays value of `dev_highlight_scalar`.  If value parameter provided then sets `dev_highlight_scalar` to value specified.




## `disconnect`

Disconnect from current game.

USAGE: `disconnect`

Cease to host or be connected to table and return to main menu.


## `displays`

Display information on currently connected displays.

USAGE: `displays`

Display information on currently connected displays.


## `double_click_container_grab`

When ON you must double-click to pick up a container (deck, stack, etc), rather than long-press.

USAGE: `double_click_container_grab [ON|OFF|TOGGLE]`

Displays value of `double_click_container_grab`.  If value parameter provided then sets `double_click_container_grab` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!double_click_container_grab` = '`double_click_container_grab TOGGLE`'


## `drawing_erase_all` (admin)

Erases all drawings.

USAGE: `drawing_erase_all`


## `drawing_render_fully_visible`

Render drawn lines without limiting against UI etc.

USAGE: `drawing_render_fully_visible [ON|OFF|TOGGLE]`

Displays value of `drawing_render_fully_visible`.  If value parameter provided then sets `drawing_render_fully_visible` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!drawing_render_fully_visible` = '`drawing_render_fully_visible TOGGLE`'


## `echo`

Echo text to the system console.

USAGE: `echo <text>`

Display the specified <text> in the System Console.


## `edit`

Edit a text variable.

USAGE: `edit <variable>`

Opens specified text variable in GUI editor.


## `end_turn`

End your turn.

USAGE: `end_turn`




## `enhanced_base_precision`

When ON the built-in models with circular bases will have more accurate colliders for the bases.
This will have a higher demand on performance.

USAGE: `enhanced_base_precision [ON|OFF|TOGGLE]`

Displays value of `enhanced_base_precision`.  If value parameter provided then sets `enhanced_base_precision` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!enhanced_base_precision` = '`enhanced_base_precision TOGGLE`'


## `errors_disable_broadcast`

When ON global errors and warnings will not be broadcast.

USAGE: `errors_disable_broadcast [ON|OFF|TOGGLE]`

Displays value of `errors_disable_broadcast`.  If value parameter provided then sets `errors_disable_broadcast` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!errors_disable_broadcast` = '`errors_disable_broadcast TOGGLE`'


## `errors_restrict_to_console`

When ON global errors and warnings will only display in the system console.

USAGE: `errors_restrict_to_console [ON|OFF|TOGGLE]`

Displays value of `errors_restrict_to_console`.  If value parameter provided then sets `errors_restrict_to_console` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!errors_restrict_to_console` = '`errors_restrict_to_console TOGGLE`'


## `escape`

Echo text variable to the system console escaped to avoid '[' formatting.

USAGE: `escape <variable>`

Display the specified <variable> in the System Console without applying any '[' format codes it contains.


## `eval`

Evaluate statement.

USAGE: `eval <variable> <statement>`

Evaluate <statement> and store result in <variable>.  <statement> can include numeric variables, vector components, arithmetic operators, and these functions:

abs, acos, asin, atan, atan2, ceil, cos, cosh, deg, exp, floor, fmod, frexp, ldexp, log, max, min, modf, pow, rad, random, sin, sinh, sqrt, tan, tanh, pi


## `examine_position`

Get position of examined component.

USAGE: `examine_position [x y z]`

Displays value of `examine_position`.

If [x y z] parameters provided then sets `examine_position` to value specified.




## `examine_rotation`

Get rotation of examined component.

USAGE: `examine_rotation [x y z]`

Displays value of `examine_rotation`.

If [x y z] parameters provided then sets `examine_rotation` to value specified.




## `exec`

Execute a series of commands.

USAGE: `exec [-q] <commands> OR exec [-q] -v <string_variable>`

Execute a string of commands separated by ';', or each line in <string_variable>, one after another.

   -q = quiet mode

   -v = variable mode

Extra commands available in a batch script:

   exit = stop processing script

   @    = use as prefix to command to silence it

   @@   = toggle every subsequent command being silent

   #    = comment

   :    = prefix to assign a label

   skip = see 'skip' command.


## `exit`

Exit batch script.

USAGE: `exit [<return value>]`

Only applicable within a script.  Stops the script execution.


## `fast_drag`

When ON activates code which attempts to reduce feeling of input lag when moving objects as client.

USAGE: `fast_drag [ON|OFF|TOGGLE]`

Displays value of `fast_drag`.  If value parameter provided then sets `fast_drag` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!fast_drag` = '`fast_drag TOGGLE`'


## `file_browser_native`

When ON uses your OS's native file browser instead of the built in one. (VR will always use the built in file browser)

USAGE: `file_browser_native [ON|OFF|TOGGLE]`

Displays value of `file_browser_native`.  If value parameter provided then sets `file_browser_native` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!file_browser_native` = '`file_browser_native TOGGLE`'


## `find` (admin)

Find a component.

USAGE: `find OR find [-c] [-name <text>] [-type <text>] [-desc <text>]`

Without parameters will return last found component (use as <<find>> in the parameter of another command).

With parameters, sets itself to first component which matches all selectors.

-c = case sensitive


## `float`

Creates a numeric variable.

USAGE: `store_number <variable> [<value>]`

Creates a numeric variable.  It will be set to <value> if it is provided, else 0.


## `fog`

When ON activates fog effect.

USAGE: `fog [ON|OFF|TOGGLE]`

Displays value of `fog`.  If value parameter provided then sets `fog` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!fog` = '`fog TOGGLE`'


## `game_hotkey_bind`

Assign key to game-defined hotkey index.

USAGE: `game_hotkey_bind <index> <key> [<key2>]`

Assign <key> to the game-defined hotkey specified by <index> (starts at 0).


## `game_hotkey_config_can_open`

When ON games may cause the [Options->Game Keys] settings window to show.

USAGE: `game_hotkey_config_can_open [ON|OFF|TOGGLE]`

Displays value of `game_hotkey_config_can_open`.  If value parameter provided then sets `game_hotkey_config_can_open` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!game_hotkey_config_can_open` = '`game_hotkey_config_can_open TOGGLE`'


## `game_hotkey_list`

List game-defined hotkeys.

USAGE: `game_hotkey_list`




## `grabbed`

GUID of first grabbed object.

Returns the GUID of the object grabbed by your pointer.


## `hand_component_hotkey_draw`

When ON pressing a number on a component which can be held in hand will draw it.

USAGE: `hand_component_hotkey_draw [ON|OFF|TOGGLE]`

Displays value of `hand_component_hotkey_draw`.  If value parameter provided then sets `hand_component_hotkey_draw` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!hand_component_hotkey_draw` = '`hand_component_hotkey_draw TOGGLE`'


## `help`

Lists all available commands or use 'help <command>' for help on a specific command.

USAGE: `help [<command> | -c]`

If <command> is provided detailed help for it is displayed, otherwise all available commands are listed.

 -c = copy all help text to clipboard


## `hidden_zone_hiding_opacity`

The opacity of hidden zones when you cannot see the objects inside them.

USAGE: `hidden_zone_hiding_opacity [value]`

Displays value of `hidden_zone_hiding_opacity`.  If value parameter provided then sets `hidden_zone_hiding_opacity` to value specified.




## `hidden_zone_showing_opacity`

The opacity of hidden zones when you can see the objects inside them.

USAGE: `hidden_zone_showing_opacity [value]`

Displays value of `hidden_zone_showing_opacity`.  If value parameter provided then sets `hidden_zone_showing_opacity` to value specified.




## `highlight` (admin)

Highlights specified component.

USAGE: `highlight <GUID> [duration] [<color>]`

Highlights specified component.  You may specify a <duration> in seconds, and a <color>.


## `host_game`

Hosts a table.

USAGE: `host_game [<seats> [<name> <password>]|[-h]] [-f]`

If <seats> is one or missing then start a singleplayer server.



<name> and <password> default to 'default_host_name' and 'default_host_password'.

-f = force (disconnect if currently hosting or connected)

-h = hotseat mode instead of multiplayer server.




## `host_max_players` (admin)

Current server max number of players.

USAGE: `host_max_players [value]`

Displays value of `host_max_players`.  If value parameter provided then sets `host_max_players` to value specified.




## `host_name` (admin)

Current server name.

USAGE: `host_name [value] OR host_name -e`

Displays value of `host_name`.  If value parameter provided then sets `host_name` to value specified.

   -e = Edit in UI editor


## `host_password` (admin)

Current server password.

USAGE: `host_password [value] OR host_password -e`

Displays value of `host_password`.  If value parameter provided then sets `host_password` to value specified.

   -e = Edit in UI editor


## `hotseat_ask_for_names`

Ask for player names when Hotseat mode begins.

USAGE: `hotseat_ask_for_names [ON|OFF|TOGGLE]`

Displays value of `hotseat_ask_for_names`.  If value parameter provided then sets `hotseat_ask_for_names` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!hotseat_ask_for_names` = '`hotseat_ask_for_names TOGGLE`'


## `hotseat_camera_reset`

Automatically reset the camera to the player's hand when the turn changes in Hotseat mode.

USAGE: `hotseat_camera_reset [ON|OFF|TOGGLE]`

Displays value of `hotseat_camera_reset`.  If value parameter provided then sets `hotseat_camera_reset` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!hotseat_camera_reset` = '`hotseat_camera_reset TOGGLE`'


## `hotseat_end_turn`

End turn in Hotseat mode.

USAGE: `hotseat_end_turn`




## `hotseat_name_1`

Player 1's name in hotseat mode.

USAGE: `hotseat_name_1 [value] OR hotseat_name_1 -e`

Displays value of `hotseat_name_1`.  If value parameter provided then sets `hotseat_name_1` to value specified.

   -e = Edit in UI editor


## `hotseat_name_2`

Player 2's name in hotseat mode.

USAGE: `hotseat_name_2 [value] OR hotseat_name_2 -e`

Displays value of `hotseat_name_2`.  If value parameter provided then sets `hotseat_name_2` to value specified.

   -e = Edit in UI editor


## `hotseat_name_3`

Player 3's name in hotseat mode.

USAGE: `hotseat_name_3 [value] OR hotseat_name_3 -e`

Displays value of `hotseat_name_3`.  If value parameter provided then sets `hotseat_name_3` to value specified.

   -e = Edit in UI editor


## `hotseat_name_4`

Player 4's name in hotseat mode.

USAGE: `hotseat_name_4 [value] OR hotseat_name_4 -e`

Displays value of `hotseat_name_4`.  If value parameter provided then sets `hotseat_name_4` to value specified.

   -e = Edit in UI editor


## `hotseat_name_5`

Player 5's name in hotseat mode.

USAGE: `hotseat_name_5 [value] OR hotseat_name_5 -e`

Displays value of `hotseat_name_5`.  If value parameter provided then sets `hotseat_name_5` to value specified.

   -e = Edit in UI editor


## `hotseat_name_6`

Player 6's name in hotseat mode.

USAGE: `hotseat_name_6 [value] OR hotseat_name_6 -e`

Displays value of `hotseat_name_6`.  If value parameter provided then sets `hotseat_name_6` to value specified.

   -e = Edit in UI editor


## `hotseat_name_7`

Player 7's name in hotseat mode.

USAGE: `hotseat_name_7 [value] OR hotseat_name_7 -e`

Displays value of `hotseat_name_7`.  If value parameter provided then sets `hotseat_name_7` to value specified.

   -e = Edit in UI editor


## `hotseat_name_8`

Player 8's name in hotseat mode.

USAGE: `hotseat_name_8 [value] OR hotseat_name_8 -e`

Displays value of `hotseat_name_8`.  If value parameter provided then sets `hotseat_name_8` to value specified.

   -e = Edit in UI editor


## `hotseat_start_turn`

Confirm start of turn in Hotseat mode.

USAGE: `hotseat_start_turn`




## `hotseat_turn_button`

When ON the button showing the current player in Hotseat mode will be displayed.

USAGE: `hotseat_turn_button [ON|OFF|TOGGLE]`

Displays value of `hotseat_turn_button`.  If value parameter provided then sets `hotseat_turn_button` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!hotseat_turn_button` = '`hotseat_turn_button TOGGLE`'


## `hotseat_turn_confirmation`

When ON you must confirm the start of your turn by clicking OK when playing in hotseat mode.

USAGE: `hotseat_turn_confirmation [ON|OFF|TOGGLE]`

Displays value of `hotseat_turn_confirmation`.  If value parameter provided then sets `hotseat_turn_confirmation` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!hotseat_turn_confirmation` = '`hotseat_turn_confirmation TOGGLE`'


## `hotseat_turn_delay`

Length of time in seconds after hitting End Turn before next player is activated in Hotseat mode.
Disabled if hotseat_turn_confirmation is ON.

USAGE: `hotseat_turn_delay [value]`

Displays value of `hotseat_turn_delay`.  If value parameter provided then sets `hotseat_turn_delay` to value specified.




## `hovered`

GUID of first object hovered over.

Returns the GUID of the first object hovered over by your pointer.


## `int`

Creates a numeric variable.

USAGE: `store_number <variable> [<value>]`

Creates a numeric variable.  It will be set to <value> if it is provided, else 0.


## `jigsaw_animate_box`

When ON jigsaw puzzle box image will be animated when appropriate.

USAGE: `jigsaw_animate_box [ON|OFF|TOGGLE]`

Displays value of `jigsaw_animate_box`.  If value parameter provided then sets `jigsaw_animate_box` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!jigsaw_animate_box` = '`jigsaw_animate_box TOGGLE`'


## `jigsaw_randomize` (admin)

Randomizes the jigsaw puzzle.

USAGE: `jigsaw_randomize`

Moves all pieces to a random position.


## `jigsaw_validate`

Validates the jigsaw puzzle.

USAGE: `jigsaw_validate`

Validates the jigsaw puzzle.


## `joystick_names`

Lists joysticks.

USAGE: `joystick_names`

Lists joysticks.


## `keyboard_single_digit_by_default`

When ON typing numbers on components will trigger the relevant action on the first digit typed, unless prefixed by a '0'

USAGE: `keyboard_single_digit_by_default [ON|OFF|TOGGLE]`

Displays value of `keyboard_single_digit_by_default`.  If value parameter provided then sets `keyboard_single_digit_by_default` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!keyboard_single_digit_by_default` = '`keyboard_single_digit_by_default TOGGLE`'


## `language`

Currently used language.

USAGE: `language [value] OR language -e`

Displays value of `language`.  If value parameter provided then sets `language` to value specified.

   -e = Edit in UI editor


## `language_arb`

Use language: Arabic. (arb))

Use `language` command variable to check current language.


## `language_bg`

Use language: Bulgarian. (bg))

Use `language` command variable to check current language.


## `language_cs`

Use language: Czech. (cs))

Use `language` command variable to check current language.


## `language_da`

Use language: Danish. (da))

Use `language` command variable to check current language.


## `language_de`

Use language: German. (de))

Use `language` command variable to check current language.


## `language_el`

Use language: Greek. (el))

Use `language` command variable to check current language.


## `language_en`

Use language: English. (en))

Use `language` command variable to check current language.


## `language_es`

Use language: Spanish. (es))

Use `language` command variable to check current language.


## `language_es_419`

Use language: Spanish (Latin America). (es-419))

Use `language` command variable to check current language.


## `language_fi`

Use language: Finnish. (fi))

Use `language` command variable to check current language.


## `language_fr`

Use language: French. (fr))

Use `language` command variable to check current language.


## `language_hu`

Use language: Hungarian. (hu))

Use `language` command variable to check current language.


## `language_it`

Use language: Italian. (it))

Use `language` command variable to check current language.


## `language_ja`

Use language: Japanese. (ja))

Use `language` command variable to check current language.


## `language_ko`

Use language: Korean. (ko))

Use `language` command variable to check current language.


## `language_nb`

Use language: Norwegian. (nb))

Use `language` command variable to check current language.


## `language_nl`

Use language: Dutch. (nl))

Use `language` command variable to check current language.


## `language_pl`

Use language: Polish. (pl))

Use `language` command variable to check current language.


## `language_pt`

Use language: Portuguese. (pt))

Use `language` command variable to check current language.


## `language_pt_br`

Use language: Portuguese (Brazil). (pt-br))

Use `language` command variable to check current language.


## `language_ro`

Use language: Romanian. (ro))

Use `language` command variable to check current language.


## `language_ru`

Use language: Russian. (ru))

Use `language` command variable to check current language.


## `language_sv`

Use language: Swedish. (sv))

Use `language` command variable to check current language.


## `language_th`

Use language: Thai. (th))

Use `language` command variable to check current language.


## `language_tr`

Use language: Turkish. (tr))

Use `language` command variable to check current language.


## `language_uk`

Use language: Ukrainian. (uk))

Use `language` command variable to check current language.


## `language_vi`

Use language: Vietnamese. (vi))

Use `language` command variable to check current language.


## `language_zh_cn`

Use language: Chinese (Simplified). (zh-cn))

Use `language` command variable to check current language.


## `language_zh_tw`

Use language: Chinese (Traditional). (zh-tw))

Use `language` command variable to check current language.


## `last`

Cannot be set; displays the last returned value.

USAGE: `last`

Displays the last returned value. Usually used by reference (i.e. <<last>>)


## `lift_height`

Lift Height when grabbing components.

USAGE: `lift_height <height>`


## `load` (admin)

Load a game.

USAGE: `load <filename>`

Load game stored as <filename>.


## `log_display_tag`

When ON displays the tag label before the log output.

USAGE: `log_display_tag [ON|OFF|TOGGLE]`

Displays value of `log_display_tag`.  If value parameter provided then sets `log_display_tag` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!log_display_tag` = '`log_display_tag TOGGLE`'


## `log_format_concise`

Sets the log formatting to concise.

USAGE: `log_format_concise`


## `log_format_expansive`

Sets the log formatting to expansive.

USAGE: `log_format_expansive`


## `log_format_truncated`

Sets the log formatting to truncated.

USAGE: `log_format_truncated`


## `log_max_table_depth`

Sets maximum depth a table in a log entry will display to.

USAGE: `log_max_table_depth [value]`

Displays value of `log_max_table_depth`.  If value parameter provided then sets `log_max_table_depth` to value specified.




## `log_output_format`

Controls how verbose logging is

USAGE: `log_output_format <format>`

<format> may be one of:

 0 = Truncated

 1 = Concise

 2 = Expansive


## `log_style_default`

Sets default styling of log entries.

USAGE: `log_style_default <color> <prefix> <postfix>`

<color> can be a named color or #RRGGBB.


## `log_style_highlight`

Sets highlight styling of log entries.

USAGE: `log_style_highlight <color> <prefix> <postfix>`

<color> can be a named color or #RRGGBB.


## `log_style_tag`

Sets the style of a log tag.  Can also be done in Lua with logStyle.

USAGE: `log_style_tag <name> <color> <prefix> <postfix>`

<color> can be a named color or #RRGGBB.


## `log_tags_clear`

Remove all defined log tags.

USAGE: `log_tags_clear`


## `log_tags_display`

Display all defined log tags.

USAGE: `log_tags_display`


## `log_tags_exclude`

When non-empty any log entries which match an excluded tag will not be displayed.

USAGE: `log_tags_exclude [value] OR log_tags_exclude -e`

Displays value of `log_tags_exclude`.  If value parameter provided then sets `log_tags_exclude` to value specified.

   -e = Edit in UI editor


## `log_tags_highlight`

When non-empty any log entry being displayed which matches a hilighted tag will be styled as such.

USAGE: `log_tags_highlight [value] OR log_tags_highlight -e`

Displays value of `log_tags_highlight`.  If value parameter provided then sets `log_tags_highlight` to value specified.

   -e = Edit in UI editor


## `log_tags_include`

When non-empty only log entries which match an included tag will be displayed.

USAGE: `log_tags_include [value] OR log_tags_include -e`

Displays value of `log_tags_include`.  If value parameter provided then sets `log_tags_include` to value specified.

   -e = Edit in UI editor


## `lua` (admin)

Execute lua statement.

USAGE: `lua <statement>`


## `measure_arrows_angle`

Angle of arrowhead prongs on Line Tool.

USAGE: `measure_arrows_angle [value]`

Displays value of `measure_arrows_angle`.  If value parameter provided then sets `measure_arrows_angle` to value specified.




## `measure_arrows_length`

Lengh of arrowhead prongs on Line Tool.

USAGE: `measure_arrows_length [value]`

Displays value of `measure_arrows_length`.  If value parameter provided then sets `measure_arrows_length` to value specified.




## `measure_components`

When ON moving a component with the Measure Movement toggle will automatically begin a measurement.

USAGE: `measure_components [ON|OFF|TOGGLE]`

Displays value of `measure_components`.  If value parameter provided then sets `measure_components` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!measure_components` = '`measure_components TOGGLE`'


## `measure_flat`

When ON measurements are flattened to the horizontal plane.  When OFF height above the table is included.

USAGE: `measure_flat [ON|OFF|TOGGLE]`

Displays value of `measure_flat`.  If value parameter provided then sets `measure_flat` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!measure_flat` = '`measure_flat TOGGLE`'


## `measure_font_size`

Size of displayed measurement when using Line Tool.

USAGE: `measure_font_size [value]`

Displays value of `measure_font_size`.  If value parameter provided then sets `measure_font_size` to value specified.




## `measure_hovered_from_edge`

When ON and you start measuring over a hovered object, the measurement will be from its edge (instead of its center).

USAGE: `measure_hovered_from_edge [ON|OFF|TOGGLE]`

Displays value of `measure_hovered_from_edge`.  If value parameter provided then sets `measure_hovered_from_edge` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!measure_hovered_from_edge` = '`measure_hovered_from_edge TOGGLE`'


## `measure_in_metric`

When ON measurements are converted to cm.

USAGE: `measure_in_metric [ON|OFF|TOGGLE]`

Displays value of `measure_in_metric`.  If value parameter provided then sets `measure_in_metric` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!measure_in_metric` = '`measure_in_metric TOGGLE`'


## `measure_inch_multiplier`

Global multiplier applied when measuring in inches.

USAGE: `measure_inch_multiplier [value]`

Displays value of `measure_inch_multiplier`.  If value parameter provided then sets `measure_inch_multiplier` to value specified.




## `measure_logging`

When ON all player measurements are logged.

USAGE: `measure_logging [ON|OFF|TOGGLE]`

Displays value of `measure_logging`.  If value parameter provided then sets `measure_logging` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!measure_logging` = '`measure_logging TOGGLE`'


## `measure_using_grid`

When ON measurements are done using grid size, rather than inches or cm.

USAGE: `measure_using_grid [ON|OFF|TOGGLE]`

Displays value of `measure_using_grid`.  If value parameter provided then sets `measure_using_grid` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!measure_using_grid` = '`measure_using_grid TOGGLE`'


## `mirror_all`

When ON mirrors to the system console any messages sent to ALL tabs.

USAGE: `mirror_all [ON|OFF|TOGGLE]`

Displays value of `mirror_all`.  If value parameter provided then sets `mirror_all` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mirror_all` = '`mirror_all TOGGLE`'


## `mirror_game`

When ON mirrors to the system console any messages sent to the GAME tab.

USAGE: `mirror_game [ON|OFF|TOGGLE]`

Displays value of `mirror_game`.  If value parameter provided then sets `mirror_game` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mirror_game` = '`mirror_game TOGGLE`'


## `mirror_global`

When ON mirrors to the system console any messages sent to the GLOBAL tab.

USAGE: `mirror_global [ON|OFF|TOGGLE]`

Displays value of `mirror_global`.  If value parameter provided then sets `mirror_global` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mirror_global` = '`mirror_global TOGGLE`'


## `mirror_team`

When ON mirrors to the system console any messages sent to the TEAM tab.

USAGE: `mirror_team [ON|OFF|TOGGLE]`

Displays value of `mirror_team`.  If value parameter provided then sets `mirror_team` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mirror_team` = '`mirror_team TOGGLE`'


## `mod_caching`

Globally control if the game should use mod caching to speed up loading. This controls regular and raw caching.

USAGE: `mod_caching [ON|OFF|TOGGLE]`

Displays value of `mod_caching`.  If value parameter provided then sets `mod_caching` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mod_caching` = '`mod_caching TOGGLE`'


## `mod_caching_raw`

This is an even faster cache than regular caching that stores the raw data for an assets, but using more disk space.

USAGE: `mod_caching_raw [ON|OFF|TOGGLE]`

Displays value of `mod_caching_raw`.  If value parameter provided then sets `mod_caching_raw` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mod_caching_raw` = '`mod_caching_raw TOGGLE`'


## `mod_thread_count`

Controls the number of threads that will be used to load up assets. Default is CPU threads - 1.

USAGE: `mod_thread_count [value]`

Displays value of `mod_thread_count`.  If value parameter provided then sets `mod_thread_count` to value specified.




## `mod_threading`

Controls if the game will use multiple threads to speed and smooth out loading of custom content. Only turn off if you have loading problems.

USAGE: `mod_threading [ON|OFF|TOGGLE]`

Displays value of `mod_threading`.  If value parameter provided then sets `mod_threading` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mod_threading` = '`mod_threading TOGGLE`'


## `mouse_shake_threshold`

Determines amount of jostling mouse requires to 'shake' held component.

USAGE: `mouse_shake_threshold [value]`

Displays value of `mouse_shake_threshold`.  If value parameter provided then sets `mouse_shake_threshold` to value specified.




## `mouse_wheel_zoom_and_center`

When ON the camera will center on the mouse pointer as you use it to zoom.

USAGE: `mouse_wheel_zoom_and_center [ON|OFF|TOGGLE]`

Displays value of `mouse_wheel_zoom_and_center`.  If value parameter provided then sets `mouse_wheel_zoom_and_center` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!mouse_wheel_zoom_and_center` = '`mouse_wheel_zoom_and_center TOGGLE`'


## `multiply`

Multiplies a numerical variable.

USAGE: `multiply <variable> <value>`

Sets <variable> to its current value * <value>.


## `music_add`

Add song to playlist.

USAGE: `music_add <url> [<name>]`

Import music file at <url> and add it to playlist.

-p = Play it.


## `music_mute`

Mute music.

USAGE: `music_mute [ON|OFF|TOGGLE]`

Displays value of `music_mute`.  If value parameter provided then sets `music_mute` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!music_mute` = '`music_mute TOGGLE`'


## `music_next`

Play next track.

USAGE: `music_next`


## `music_pause`

Pause music.

USAGE: `music_pause`


## `music_play`

Play music.

USAGE: `music_play`


## `music_prev`

Play previous track.

USAGE: `music_prev`


## `music_repeat`

Music player song repeat.

USAGE: `music_repeat [ON|OFF|TOGGLE]`

Displays value of `music_repeat`.  If value parameter provided then sets `music_repeat` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!music_repeat` = '`music_repeat TOGGLE`'


## `music_shuffle`

Music player playlist shuffle.

USAGE: `music_shuffle [ON|OFF|TOGGLE]`

Displays value of `music_shuffle`.  If value parameter provided then sets `music_shuffle` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!music_shuffle` = '`music_shuffle TOGGLE`'


## `music_timecode`

Current timecode of music (seconds).

USAGE: `music_timecode [value]`

Displays value of `music_timecode`.  If value parameter provided then sets `music_timecode` to value specified.




## `music_volume`

The volume of the music player.

USAGE: `music_volume [value]`

Displays value of `music_volume`.  If value parameter provided then sets `music_volume` to value specified.




## `negative_typed_numbers`

When ON pressing `Minus` before typing a number on component will enter a negative number.  Remember to unbind the `Minus` key from Scale Down!

USAGE: `negative_typed_numbers [ON|OFF|TOGGLE]`

Displays value of `negative_typed_numbers`.  If value parameter provided then sets `negative_typed_numbers` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!negative_typed_numbers` = '`negative_typed_numbers TOGGLE`'


## `pointer_position`

Get position of player pointer.

USAGE: `pointer_position [x y z]`

Displays value of `pointer_position`.

If [x y z] parameters provided then sets `pointer_position` to value specified.




## `pure_fog`

When ON display floor mist when in Pure Mode.

USAGE: `pure_fog [ON|OFF|TOGGLE]`

Displays value of `pure_fog`.  If value parameter provided then sets `pure_fog` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!pure_fog` = '`pure_fog TOGGLE`'


## `pure_mode`

When ON use Pure Mode visual style, colours for which can be set in the Theme Editor.

USAGE: `pure_mode [ON|OFF|TOGGLE]`

Displays value of `pure_mode`.  If value parameter provided then sets `pure_mode` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!pure_mode` = '`pure_mode TOGGLE`'


## `pure_override_custom_table`

When ON images on custom tables will be hidden while in Pure Mode.

USAGE: `pure_override_custom_table [ON|OFF|TOGGLE]`

Displays value of `pure_override_custom_table`.  If value parameter provided then sets `pure_override_custom_table` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!pure_override_custom_table` = '`pure_override_custom_table TOGGLE`'


## `pure_specular_intensity_a`

The specular intensity of the primary table color when in Pure Mode (0.0 - 1.0).

USAGE: `pure_specular_intensity_a [value]`

Displays value of `pure_specular_intensity_a`.  If value parameter provided then sets `pure_specular_intensity_a` to value specified.




## `pure_specular_intensity_b`

The specular intensity of the secondary table color when in Pure Mode (0.0 - 1.0).

USAGE: `pure_specular_intensity_b [value]`

Displays value of `pure_specular_intensity_b`.  If value parameter provided then sets `pure_specular_intensity_b` to value specified.




## `pure_specular_intensity_splash`

The specular intensity of the splash table color when in Pure Mode (0.0 - 1.0).

USAGE: `pure_specular_intensity_splash [value]`

Displays value of `pure_specular_intensity_splash`.  If value parameter provided then sets `pure_specular_intensity_splash` to value specified.




## `pure_specular_sharpness_a`

The specular sharpness of the primary table color when in Pure Mode (2.0 - 8.0).

USAGE: `pure_specular_sharpness_a [value]`

Displays value of `pure_specular_sharpness_a`.  If value parameter provided then sets `pure_specular_sharpness_a` to value specified.




## `pure_specular_sharpness_b`

The specular sharness of the secondary table color when in Pure Mode (2.0 - 8.0).

USAGE: `pure_specular_sharpness_b [value]`

Displays value of `pure_specular_sharpness_b`.  If value parameter provided then sets `pure_specular_sharpness_b` to value specified.




## `pure_specular_sharpness_splash`

The specular sharness of the splash table color when in Pure Mode (2.0 - 8.0).

USAGE: `pure_specular_sharpness_splash [value]`

Displays value of `pure_specular_sharpness_splash`.  If value parameter provided then sets `pure_specular_sharpness_splash` to value specified.




## `quiet_mode`

When ON commands display their outputs only.

USAGE: `quiet_mode [ON|OFF|TOGGLE]`

Displays value of `quiet_mode`.  If value parameter provided then sets `quiet_mode` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!quiet_mode` = '`quiet_mode TOGGLE`'


## `quit`

Exit TTS entirely.

USAGE: `quit [-f]`

Exit to desktop.  Shows a confirm prompt.

 -f = Don't show prompt: force exit.


## `randomize_zone_prompt_on_load`

When ON and you load a game with a Randomize Zone, it will ask if you want to activate it.

USAGE: `randomize_zone_prompt_on_load [ON|OFF|TOGGLE]`

Displays value of `randomize_zone_prompt_on_load`.  If value parameter provided then sets `randomize_zone_prompt_on_load` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!randomize_zone_prompt_on_load` = '`randomize_zone_prompt_on_load TOGGLE`'


## `reset`

Resets a persistent variable to its default value and removes its stored setting (playerpref).

USAGE: `reset <variable>`

Resets a variable.  May only reset variables which are persistent.


## `rewind_interval`

Time in seconds between each rewind.  If set to 0 then rewind is disabled.

USAGE: `rewind_interval [value]`

Displays value of `rewind_interval`.  If value parameter provided then sets `rewind_interval` to value specified.




## `rotation_degrees`

Degrees component is rotate through when held.

USAGE: `rotation_degrees <degrees>`

Must be a mulitple of 15


## `run`

Execute a series of commands.

USAGE: `exec [-q] <commands> OR exec [-q] -v <string_variable>`

Execute a string of commands separated by ';', or each line in <string_variable>, one after another.

   -q = quiet mode

   -v = variable mode

Extra commands available in a batch script:

   exit = stop processing script

   @    = use as prefix to command to silence it

   @@   = toggle every subsequent command being silent

   #    = comment

   :    = prefix to assign a label

   skip = see 'skip' command.


## `save` (admin)

Save current game.

USAGE: `save <filename> [<gamename>]`

Saves game as <filename>.  Optionally provide a <gamename>.


## `say_game`

Send text as if typed into Game tab.

USAGE: `say_game <message>`

Sends <message> to Game tab as if you had typed it in.


## `say_global`

Send text as if typed into Global tab.

USAGE: `say_global <message>`

Sends <message> to Global tab as if you had typed it in.


## `say_team`

Send text as if typed into Team tab.

USAGE: `say_team <message>`

Sends <message> to Team tab as if you had typed it in.


## `search_close_after_take`

If ON then the search interface will close as soon as you take any object from it.

USAGE: `search_close_after_take [ON|OFF|TOGGLE]`

Displays value of `search_close_after_take`.  If value parameter provided then sets `search_close_after_take` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!search_close_after_take` = '`search_close_after_take TOGGLE`'


## `search_specularity_threshold`

Sets the threshold below which specularity is disabled for objects in containers, so as not to appear faded.

USAGE: `search_specularity_threshold [value]`

Displays value of `search_specularity_threshold`.  If value parameter provided then sets `search_specularity_threshold` to value specified.




## `sendkey`

Emulates a keypress (or other input).

USAGE: `sendkey <key>`

Emulates Unity KeyCode <key> as if it were pressed by the user.


## `skip`

Skip forward in batch script.

USAGE: `skip <label> [<variable> [<comparison> <value> [threshold]]]`

Only applicable within a script.  If only <label> specified, or <variable> (or its <comparison> to <value>) is positive, then skip ahead to <label>.

If <threshold> specified then = and <> will use it.Comparisons: = < > <= >= <>


## `spectator_activate_with_resolution`

Activates spectator window with specified resolution.

USAGE: `spectator_activate_with_resolution <width> <height> [-d <display>] [-r <rate>] [-p <x> <y>]`

Activates spectator window with specified resolution.

-d = specify display number (use `displays` command to list displays)

-p = display in a panel inside TTS instead of on a separate display

-o = no overlay buttons

-s = no sizing corners

-l = locked in place (not draggable with mouse)




## `spectator_camera_attachment`

<GUID> of component or <PLAYER COLOR> of pointer which spectator camera will follow when spectator_camera_follow_attachment is ON.

USAGE: `spectator_camera_attachment [value] OR spectator_camera_attachment -e`

Displays value of `spectator_camera_attachment`.  If value parameter provided then sets `spectator_camera_attachment` to value specified.

   -e = Edit in UI editor


## `spectator_camera_dolly`

Set distance camera is offset when following a component, along its facing direction.

USAGE: `spectator_camera_dolly [value]`

Displays value of `spectator_camera_dolly`.  If value parameter provided then sets `spectator_camera_dolly` to value specified.




## `spectator_camera_follow_attachment`

Set spectator camera to follow component or player pointer specified with spectator_camera_attachment.

USAGE: `spectator_camera_follow_attachment [ON|OFF|TOGGLE]`

Displays value of `spectator_camera_follow_attachment`.  If value parameter provided then sets `spectator_camera_follow_attachment` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_camera_follow_attachment` = '`spectator_camera_follow_attachment TOGGLE`'


## `spectator_camera_follow_player`

Set spectator camera to follow player camera.

USAGE: `spectator_camera_follow_player [ON|OFF|TOGGLE]`

Displays value of `spectator_camera_follow_player`.  If value parameter provided then sets `spectator_camera_follow_player` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_camera_follow_player` = '`spectator_camera_follow_player TOGGLE`'


## `spectator_camera_load`

Set spectator camera position to saved position.

USAGE: `spectator_camera_load [value]`

Displays value of `spectator_camera_load`.  If value parameter provided then sets `spectator_camera_load` to value specified.




## `spectator_camera_load_zero`

Set spectator camera position to saved position.  Position is zero-indexed (so one less than displayed in UI)

USAGE: `spectator_camera_load_zero [value]`

Displays value of `spectator_camera_load_zero`.  If value parameter provided then sets `spectator_camera_load_zero` to value specified.




## `spectator_camera_look_at`

Make spectator camera look at a component or player pointer.

USAGE: `spectator_camera_look_at <GUID> OR spectator_camera_look_at <COLOR>`


## `spectator_camera_offset_position`

Set camera positional offset from component.

USAGE: `spectator_camera_offset_position [x y z]`

Displays value of `spectator_camera_offset_position`.

If [x y z] parameters provided then sets `spectator_camera_offset_position` to value specified.




## `spectator_camera_offset_rotation`

Set camera rotational offset from component.

USAGE: `spectator_camera_offset_rotation [x y z]`

Displays value of `spectator_camera_offset_rotation`.

If [x y z] parameters provided then sets `spectator_camera_offset_rotation` to value specified.




## `spectator_camera_override_player_with_look`

When ON the look and track commands will work when spectator_camera_follow_player is ON.

USAGE: `spectator_camera_override_player_with_look [ON|OFF|TOGGLE]`

Displays value of `spectator_camera_override_player_with_look`.  If value parameter provided then sets `spectator_camera_override_player_with_look` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_camera_override_player_with_look` = '`spectator_camera_override_player_with_look TOGGLE`'


## `spectator_camera_smooth_on_load`

Set spectator camera to follow player camera.

USAGE: `spectator_camera_smooth_on_load [ON|OFF|TOGGLE]`

Displays value of `spectator_camera_smooth_on_load`.  If value parameter provided then sets `spectator_camera_smooth_on_load` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_camera_smooth_on_load` = '`spectator_camera_smooth_on_load TOGGLE`'


## `spectator_camera_smooth_position`

The factor used to smooth the spectator camera follow position.

USAGE: `spectator_camera_smooth_position [value]`

Displays value of `spectator_camera_smooth_position`.  If value parameter provided then sets `spectator_camera_smooth_position` to value specified.




## `spectator_camera_smooth_rotation`

The factor used to smooth the spectator camera follow rotation.

USAGE: `spectator_camera_smooth_rotation [value]`

Displays value of `spectator_camera_smooth_rotation`.  If value parameter provided then sets `spectator_camera_smooth_rotation` to value specified.




## `spectator_camera_stay_upright`

When ON the camera will not rotate upside-down.

USAGE: `spectator_camera_stay_upright [ON|OFF|TOGGLE]`

Displays value of `spectator_camera_stay_upright`.  If value parameter provided then sets `spectator_camera_stay_upright` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_camera_stay_upright` = '`spectator_camera_stay_upright TOGGLE`'


## `spectator_camera_target`

<GUID> or <PLAYER COLOR> for spectator camera to look at.

USAGE: `spectator_camera_target [value] OR spectator_camera_target -e`

Displays value of `spectator_camera_target`.  If value parameter provided then sets `spectator_camera_target` to value specified.

   -e = Edit in UI editor


## `spectator_camera_tracking`

When ON spectator camera willo track target specified with spectator_camera_target.

USAGE: `spectator_camera_tracking [ON|OFF|TOGGLE]`

Displays value of `spectator_camera_tracking`.  If value parameter provided then sets `spectator_camera_tracking` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_camera_tracking` = '`spectator_camera_tracking TOGGLE`'


## `spectator_panel_buttons`

When ON the spectator panel will have overlay buttons (copy player, lock to player, restrict view, close).

USAGE: `spectator_panel_buttons [ON|OFF|TOGGLE]`

Displays value of `spectator_panel_buttons`.  If value parameter provided then sets `spectator_panel_buttons` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_panel_buttons` = '`spectator_panel_buttons TOGGLE`'


## `spectator_panel_corners`

When ON the spectator panel will have draggable corners (allows resizing).

USAGE: `spectator_panel_corners [ON|OFF|TOGGLE]`

Displays value of `spectator_panel_corners`.  If value parameter provided then sets `spectator_panel_corners` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_panel_corners` = '`spectator_panel_corners TOGGLE`'


## `spectator_panel_locked`

When ON the spectaor panel will not be draggable with the mouse.

USAGE: `spectator_panel_locked [ON|OFF|TOGGLE]`

Displays value of `spectator_panel_locked`.  If value parameter provided then sets `spectator_panel_locked` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_panel_locked` = '`spectator_panel_locked TOGGLE`'


## `spectator_post_processing`

When ON the spectator window will apply post-processing effects.

USAGE: `spectator_post_processing [ON|OFF|TOGGLE]`

Displays value of `spectator_post_processing`.  If value parameter provided then sets `spectator_post_processing` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_post_processing` = '`spectator_post_processing TOGGLE`'


## `spectator_restrict_view`

When ON the spectator window will only see what attached spectators see.

USAGE: `spectator_restrict_view [ON|OFF|TOGGLE]`

Displays value of `spectator_restrict_view`.  If value parameter provided then sets `spectator_restrict_view` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_restrict_view` = '`spectator_restrict_view TOGGLE`'


## `spectator_restrict_zoom`

When ON the spectator zoom display will be restricted if the view is restricted.

USAGE: `spectator_restrict_zoom [ON|OFF|TOGGLE]`

Displays value of `spectator_restrict_zoom`.  If value parameter provided then sets `spectator_restrict_zoom` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_restrict_zoom` = '`spectator_restrict_zoom TOGGLE`'


## `spectator_screen`

When ON the spectator view will be displayed on a screen.

USAGE: `spectator_screen [ON|OFF|TOGGLE]`

Displays value of `spectator_screen`.  If value parameter provided then sets `spectator_screen` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_screen` = '`spectator_screen TOGGLE`'


## `spectator_show_game_ui`

When ON the spectator window will display UI elements created by the currently loaded game.

USAGE: `spectator_show_game_ui [ON|OFF|TOGGLE]`

Displays value of `spectator_show_game_ui`.  If value parameter provided then sets `spectator_show_game_ui` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_show_game_ui` = '`spectator_show_game_ui TOGGLE`'


## `spectator_show_grid`

When ON the spectator window will display grid lines.

USAGE: `spectator_show_grid [ON|OFF|TOGGLE]`

Displays value of `spectator_show_grid`.  If value parameter provided then sets `spectator_show_grid` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_show_grid` = '`spectator_show_grid TOGGLE`'


## `spectator_show_ui`

When ON the spectator window will display UI elements.

USAGE: `spectator_show_ui [ON|OFF|TOGGLE]`

Displays value of `spectator_show_ui`.  If value parameter provided then sets `spectator_show_ui` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_show_ui` = '`spectator_show_ui TOGGLE`'


## `spectator_show_zoom`

When ON the spectator window will show the alt zoom display.

USAGE: `spectator_show_zoom [ON|OFF|TOGGLE]`

Displays value of `spectator_show_zoom`.  If value parameter provided then sets `spectator_show_zoom` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_show_zoom` = '`spectator_show_zoom TOGGLE`'


## `spectator_window`

When ON the spectator view will be displayed in a window inside TTS.

USAGE: `spectator_window [ON|OFF|TOGGLE]`

Displays value of `spectator_window`.  If value parameter provided then sets `spectator_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_window` = '`spectator_window TOGGLE`'


## `spectator_zoom_follows_pointer`

When ON the spectator zoom display will appear at the pointer location. When OFF it will appear at spectator_zoom_position.

USAGE: `spectator_zoom_follows_pointer [ON|OFF|TOGGLE]`

Displays value of `spectator_zoom_follows_pointer`.  If value parameter provided then sets `spectator_zoom_follows_pointer` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!spectator_zoom_follows_pointer` = '`spectator_zoom_follows_pointer TOGGLE`'


## `spectator_zoom_position`

The location the zoom display will appear when spectator_zoom_follows_pointer is off.  0,0 = bottom left, 1,1 = top right.

USAGE: `spectator_zoom_position [value]`

Display value of spectator_zoom_position.  If value parameter provided then sets spectator_zoom_position to value specified.


## `stats_monitor`

When ON activates stats monitor.

USAGE: `stats_monitor [ON|OFF|TOGGLE]`

Displays value of `stats_monitor`.  If value parameter provided then sets `stats_monitor` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!stats_monitor` = '`stats_monitor TOGGLE`'


## `status`

Displays current status.

USAGE: `status`

Displays information on current game state.


## `store_number`

Creates a numeric variable.

USAGE: `store_number <variable> [<value>]`

Creates a numeric variable.  It will be set to <value> if it is provided, else 0.


## `store_text`

Creates a text variable.

USAGE: `store_text <variable> [<value>]`

Creates a text variable.  It will be set to <value> if it is provided.

If in a multiline batch (such as autoexec), leaving value blank will set

it to the block of text which follows, until 'end <variable>'


## `store_toggle`

Creates a variable which can be ON or OFF.

USAGE: `store_toggle <variable> [<value>]`

Creates a variable which can be ON or OFF.  It will be set to <value> if it is provided, else OFF.


## `string`

Creates a text variable.

USAGE: `store_text <variable> [<value>]`

Creates a text variable.  It will be set to <value> if it is provided.

If in a multiline batch (such as autoexec), leaving value blank will set

it to the block of text which follows, until 'end <variable>'


## `subtract`

Set a numerical variable to itself subtracted from a value.

USAGE: `subtract <variable> <value>`

Sets <variable> to <value> - current value.


## `team`

Your current team.

USAGE: `team [<team>]`

Returns your current team.  If <team> provided will attempt to swap you to that team.


## `timestamp_all`

When ON timestamps will be displayed for ALL messages.

USAGE: `timestamp_all [ON|OFF|TOGGLE]`

Displays value of `timestamp_all`.  If value parameter provided then sets `timestamp_all` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!timestamp_all` = '`timestamp_all TOGGLE`'


## `timestamp_format`

Format string which controls how message timestamps are displayed.  See tinyurl.com/ycwh45af for details.

USAGE: `timestamp_format [value] OR timestamp_format -e`

Displays value of `timestamp_format`.  If value parameter provided then sets `timestamp_format` to value specified.

   -e = Edit in UI editor


## `timestamp_game`

When ON timestamps will be displayed for GAME chat messages.

USAGE: `timestamp_game [ON|OFF|TOGGLE]`

Displays value of `timestamp_game`.  If value parameter provided then sets `timestamp_game` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!timestamp_game` = '`timestamp_game TOGGLE`'


## `timestamp_global`

When ON timestamps will be displayed for GLOBAL chat messages.

USAGE: `timestamp_global [ON|OFF|TOGGLE]`

Displays value of `timestamp_global`.  If value parameter provided then sets `timestamp_global` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!timestamp_global` = '`timestamp_global TOGGLE`'


## `timestamp_system`

When ON timestamps will be displayed for SYSTEM messages.

USAGE: `timestamp_system [ON|OFF|TOGGLE]`

Displays value of `timestamp_system`.  If value parameter provided then sets `timestamp_system` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!timestamp_system` = '`timestamp_system TOGGLE`'


## `timestamp_team`

When ON timestamps will be displayed for TEAM chat messages.

USAGE: `timestamp_team [ON|OFF|TOGGLE]`

Displays value of `timestamp_team`.  If value parameter provided then sets `timestamp_team` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!timestamp_team` = '`timestamp_team TOGGLE`'


## `tool_attach`

Change tool mode to attach.

USAGE: `tool_attach`

Changes current tool mode to attach.


## `tool_current`

Change or displays the current tool mode.

USAGE: `tool_current [mode]`

Displays index of current tool mode.  If mode specified then changes to it.


## `tool_decal`

Change tool mode to decal.

USAGE: `tool_decal`

Changes current tool mode to decal.


## `tool_erase`

Change tool mode to erase.

USAGE: `tool_erase`

Changes current tool mode to erase.


## `tool_fixed_joint`

Change tool mode to fixed_joint.

USAGE: `tool_fixed_joint`

Changes current tool mode to fixed_joint.


## `tool_flick`

Change tool mode to flick.

USAGE: `tool_flick`

Changes current tool mode to flick.


## `tool_fog_of_war`

Change tool mode to fog_of_war.

USAGE: `tool_fog_of_war`

Changes current tool mode to fog_of_war.


## `tool_grab`

Change tool mode to grab.

USAGE: `tool_grab`

Changes current tool mode to grab.


## `tool_hands`

Change tool mode to hands.

USAGE: `tool_hands`

Changes current tool mode to hands.


## `tool_hidden`

Change tool mode to hidden.

USAGE: `tool_hidden`

Changes current tool mode to hidden.


## `tool_hinge_joint`

Change tool mode to hinge_joint.

USAGE: `tool_hinge_joint`

Changes current tool mode to hinge_joint.


## `tool_layout_zone`

Change tool mode to layout_zone.

USAGE: `tool_layout_zone`

Changes current tool mode to layout_zone.


## `tool_line`

Change tool mode to line.

USAGE: `tool_line`

Changes current tool mode to line.


## `tool_move`

Change tool mode to move.

USAGE: `tool_move`

Changes current tool mode to move.


## `tool_paint`

Change tool mode to paint.

USAGE: `tool_paint`

Changes current tool mode to paint.


## `tool_randomize`

Change tool mode to randomize.

USAGE: `tool_randomize`

Changes current tool mode to randomize.


## `tool_revert`

Change tool mode.

USAGE: `tool_revert [-d]`

Changes current tool mode to that which was in use prior to last tool switch.  -d = If last switch was to the same tool then don't change


## `tool_rotate`

Change tool mode to rotate.

USAGE: `tool_rotate`

Changes current tool mode to rotate.


## `tool_rotation_value`

Change tool mode to rotation_value.

USAGE: `tool_rotation_value`

Changes current tool mode to rotation_value.


## `tool_scale`

Change tool mode to scale.

USAGE: `tool_scale`

Changes current tool mode to scale.


## `tool_scripting`

Change tool mode to scripting.

USAGE: `tool_scripting`

Changes current tool mode to scripting.


## `tool_snap`

Change tool mode to snap.

USAGE: `tool_snap`

Changes current tool mode to snap.


## `tool_snap_rotate`

Change tool mode to snap_rotate.

USAGE: `tool_snap_rotate`

Changes current tool mode to snap_rotate.


## `tool_spawn`

Change tool mode to spawn.

USAGE: `tool_spawn`

Changes current tool mode to spawn.


## `tool_spring_joint`

Change tool mode to spring_joint.

USAGE: `tool_spring_joint`

Changes current tool mode to spring_joint.


## `tool_text`

Change tool mode to text.

USAGE: `tool_text`

Changes current tool mode to text.


## `tool_vector`

Change tool mode to vector.

USAGE: `tool_vector`

Changes current tool mode to vector.


## `tool_vector_box`

Change tool mode to vector_box.

USAGE: `tool_vector_box`

Changes current tool mode to vector_box.


## `tool_vector_circle`

Change tool mode to vector_circle.

USAGE: `tool_vector_circle`

Changes current tool mode to vector_circle.


## `tool_vector_erase`

Change tool mode to vector_erase.

USAGE: `tool_vector_erase`

Changes current tool mode to vector_erase.


## `tool_vector_line`

Change tool mode to vector_line.

USAGE: `tool_vector_line`

Changes current tool mode to vector_line.


## `tool_vector_pixel`

Change tool mode to vector_pixel.

USAGE: `tool_vector_pixel`

Changes current tool mode to vector_pixel.


## `tool_volume_scale`

Change tool mode to volume_scale.

USAGE: `tool_volume_scale`

Changes current tool mode to volume_scale.


## `translate`

Translate supplied English text into current language if it exist in TTS localization dictionary.

USAGE: `translate <text>`


## `translation_export`

Export language translation as CSV.

USAGE: `translation_export <language> <filename>`

Save language translations for specified <language> in CSV file <filename>.


## `translation_for_arb`

Filename of translation CSV for language: Arabic. (arb))

USAGE: `translation_for_arb [value] OR translation_for_arb -e`

Displays value of `translation_for_arb`.  If value parameter provided then sets `translation_for_arb` to value specified.

   -e = Edit in UI editor


## `translation_for_bg`

Filename of translation CSV for language: Bulgarian. (bg))

USAGE: `translation_for_bg [value] OR translation_for_bg -e`

Displays value of `translation_for_bg`.  If value parameter provided then sets `translation_for_bg` to value specified.

   -e = Edit in UI editor


## `translation_for_cs`

Filename of translation CSV for language: Czech. (cs))

USAGE: `translation_for_cs [value] OR translation_for_cs -e`

Displays value of `translation_for_cs`.  If value parameter provided then sets `translation_for_cs` to value specified.

   -e = Edit in UI editor


## `translation_for_da`

Filename of translation CSV for language: Danish. (da))

USAGE: `translation_for_da [value] OR translation_for_da -e`

Displays value of `translation_for_da`.  If value parameter provided then sets `translation_for_da` to value specified.

   -e = Edit in UI editor


## `translation_for_de`

Filename of translation CSV for language: German. (de))

USAGE: `translation_for_de [value] OR translation_for_de -e`

Displays value of `translation_for_de`.  If value parameter provided then sets `translation_for_de` to value specified.

   -e = Edit in UI editor


## `translation_for_el`

Filename of translation CSV for language: Greek. (el))

USAGE: `translation_for_el [value] OR translation_for_el -e`

Displays value of `translation_for_el`.  If value parameter provided then sets `translation_for_el` to value specified.

   -e = Edit in UI editor


## `translation_for_en`

Filename of translation CSV for language: English. (en))

USAGE: `translation_for_en [value] OR translation_for_en -e`

Displays value of `translation_for_en`.  If value parameter provided then sets `translation_for_en` to value specified.

   -e = Edit in UI editor


## `translation_for_es`

Filename of translation CSV for language: Spanish. (es))

USAGE: `translation_for_es [value] OR translation_for_es -e`

Displays value of `translation_for_es`.  If value parameter provided then sets `translation_for_es` to value specified.

   -e = Edit in UI editor


## `translation_for_es_419`

Filename of translation CSV for language: Spanish (Latin America). (es-419))

USAGE: `translation_for_es_419 [value] OR translation_for_es_419 -e`

Displays value of `translation_for_es_419`.  If value parameter provided then sets `translation_for_es_419` to value specified.

   -e = Edit in UI editor


## `translation_for_fi`

Filename of translation CSV for language: Finnish. (fi))

USAGE: `translation_for_fi [value] OR translation_for_fi -e`

Displays value of `translation_for_fi`.  If value parameter provided then sets `translation_for_fi` to value specified.

   -e = Edit in UI editor


## `translation_for_fr`

Filename of translation CSV for language: French. (fr))

USAGE: `translation_for_fr [value] OR translation_for_fr -e`

Displays value of `translation_for_fr`.  If value parameter provided then sets `translation_for_fr` to value specified.

   -e = Edit in UI editor


## `translation_for_hu`

Filename of translation CSV for language: Hungarian. (hu))

USAGE: `translation_for_hu [value] OR translation_for_hu -e`

Displays value of `translation_for_hu`.  If value parameter provided then sets `translation_for_hu` to value specified.

   -e = Edit in UI editor


## `translation_for_it`

Filename of translation CSV for language: Italian. (it))

USAGE: `translation_for_it [value] OR translation_for_it -e`

Displays value of `translation_for_it`.  If value parameter provided then sets `translation_for_it` to value specified.

   -e = Edit in UI editor


## `translation_for_ja`

Filename of translation CSV for language: Japanese. (ja))

USAGE: `translation_for_ja [value] OR translation_for_ja -e`

Displays value of `translation_for_ja`.  If value parameter provided then sets `translation_for_ja` to value specified.

   -e = Edit in UI editor


## `translation_for_ko`

Filename of translation CSV for language: Korean. (ko))

USAGE: `translation_for_ko [value] OR translation_for_ko -e`

Displays value of `translation_for_ko`.  If value parameter provided then sets `translation_for_ko` to value specified.

   -e = Edit in UI editor


## `translation_for_nb`

Filename of translation CSV for language: Norwegian. (nb))

USAGE: `translation_for_nb [value] OR translation_for_nb -e`

Displays value of `translation_for_nb`.  If value parameter provided then sets `translation_for_nb` to value specified.

   -e = Edit in UI editor


## `translation_for_nl`

Filename of translation CSV for language: Dutch. (nl))

USAGE: `translation_for_nl [value] OR translation_for_nl -e`

Displays value of `translation_for_nl`.  If value parameter provided then sets `translation_for_nl` to value specified.

   -e = Edit in UI editor


## `translation_for_pl`

Filename of translation CSV for language: Polish. (pl))

USAGE: `translation_for_pl [value] OR translation_for_pl -e`

Displays value of `translation_for_pl`.  If value parameter provided then sets `translation_for_pl` to value specified.

   -e = Edit in UI editor


## `translation_for_pt`

Filename of translation CSV for language: Portuguese. (pt))

USAGE: `translation_for_pt [value] OR translation_for_pt -e`

Displays value of `translation_for_pt`.  If value parameter provided then sets `translation_for_pt` to value specified.

   -e = Edit in UI editor


## `translation_for_pt_br`

Filename of translation CSV for language: Portuguese (Brazil). (pt-br))

USAGE: `translation_for_pt_br [value] OR translation_for_pt_br -e`

Displays value of `translation_for_pt_br`.  If value parameter provided then sets `translation_for_pt_br` to value specified.

   -e = Edit in UI editor


## `translation_for_ro`

Filename of translation CSV for language: Romanian. (ro))

USAGE: `translation_for_ro [value] OR translation_for_ro -e`

Displays value of `translation_for_ro`.  If value parameter provided then sets `translation_for_ro` to value specified.

   -e = Edit in UI editor


## `translation_for_ru`

Filename of translation CSV for language: Russian. (ru))

USAGE: `translation_for_ru [value] OR translation_for_ru -e`

Displays value of `translation_for_ru`.  If value parameter provided then sets `translation_for_ru` to value specified.

   -e = Edit in UI editor


## `translation_for_sv`

Filename of translation CSV for language: Swedish. (sv))

USAGE: `translation_for_sv [value] OR translation_for_sv -e`

Displays value of `translation_for_sv`.  If value parameter provided then sets `translation_for_sv` to value specified.

   -e = Edit in UI editor


## `translation_for_th`

Filename of translation CSV for language: Thai. (th))

USAGE: `translation_for_th [value] OR translation_for_th -e`

Displays value of `translation_for_th`.  If value parameter provided then sets `translation_for_th` to value specified.

   -e = Edit in UI editor


## `translation_for_tr`

Filename of translation CSV for language: Turkish. (tr))

USAGE: `translation_for_tr [value] OR translation_for_tr -e`

Displays value of `translation_for_tr`.  If value parameter provided then sets `translation_for_tr` to value specified.

   -e = Edit in UI editor


## `translation_for_uk`

Filename of translation CSV for language: Ukrainian. (uk))

USAGE: `translation_for_uk [value] OR translation_for_uk -e`

Displays value of `translation_for_uk`.  If value parameter provided then sets `translation_for_uk` to value specified.

   -e = Edit in UI editor


## `translation_for_vi`

Filename of translation CSV for language: Vietnamese. (vi))

USAGE: `translation_for_vi [value] OR translation_for_vi -e`

Displays value of `translation_for_vi`.  If value parameter provided then sets `translation_for_vi` to value specified.

   -e = Edit in UI editor


## `translation_for_zh_cn`

Filename of translation CSV for language: Chinese (Simplified). (zh-cn))

USAGE: `translation_for_zh_cn [value] OR translation_for_zh_cn -e`

Displays value of `translation_for_zh_cn`.  If value parameter provided then sets `translation_for_zh_cn` to value specified.

   -e = Edit in UI editor


## `translation_for_zh_tw`

Filename of translation CSV for language: Chinese (Traditional). (zh-tw))

USAGE: `translation_for_zh_tw [value] OR translation_for_zh_tw -e`

Displays value of `translation_for_zh_tw`.  If value parameter provided then sets `translation_for_zh_tw` to value specified.

   -e = Edit in UI editor


## `translation_import`

Import language translations in CSV.

USAGE: `translation_import <filename>`

Load all language translations in CSV file <filename>.


## `ui_anchor`

Set position on screen UI elements will be created relative to.

USAGE: `ui_anchor [value]`

Display value of ui_anchor.  If value parameter provided then sets ui_anchor to value specified.


## `ui_autofocus_search`

Automatically focus search input boxes when windows containing them are displayed.

USAGE: `ui_autofocus_search [ON|OFF|TOGGLE]`

Displays value of `ui_autofocus_search`.  If value parameter provided then sets `ui_autofocus_search` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_autofocus_search` = '`ui_autofocus_search TOGGLE`'


## `ui_book_buttons_on_hover`

Whether books only show their attached buttons when hovered (if OFF then they show them all the time).

USAGE: `ui_book_buttons_on_hover [ON|OFF|TOGGLE]`

Displays value of `ui_book_buttons_on_hover`.  If value parameter provided then sets `ui_book_buttons_on_hover` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_book_buttons_on_hover` = '`ui_book_buttons_on_hover TOGGLE`'


## `ui_book_highlight_color`

Color of highlighter on book pop-out.

USAGE: `ui_book_highlight_color [value] OR ui_book_highlight_color -e`

Displays value of `ui_book_highlight_color`.  If value parameter provided then sets `ui_book_highlight_color` to value specified.

   -e = Edit in UI editor


## `ui_book_navigation_bookmark_level`

Level of bookmarks which navigation buttons will jump between.  If 0 then ui_book_navigation_step will always be used.

USAGE: `ui_book_navigation_bookmark_level [value]`

Displays value of `ui_book_navigation_bookmark_level`.  If value parameter provided then sets `ui_book_navigation_bookmark_level` to value specified.




## `ui_book_navigation_step`

Number of pages the back and forward buttons on the book reader will jump.

USAGE: `ui_book_navigation_step [value]`

Displays value of `ui_book_navigation_step`.  If value parameter provided then sets `ui_book_navigation_step` to value specified.




## `ui_book_page_opacity`

Opacity of book pop-out pages when you are not hovering over them.

USAGE: `ui_book_page_opacity [value]`

Displays value of `ui_book_page_opacity`.  If value parameter provided then sets `ui_book_page_opacity` to value specified.




## `ui_book_panel_opacity`

Opacity of book pop-out panel and buttons when you are not hovering over it.

USAGE: `ui_book_panel_opacity [value]`

Displays value of `ui_book_panel_opacity`.  If value parameter provided then sets `ui_book_panel_opacity` to value specified.




## `ui_book_window`

When ON the book pop-out window is active.

USAGE: `ui_book_window [ON|OFF|TOGGLE]`

Displays value of `ui_book_window`.  If value parameter provided then sets `ui_book_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_book_window` = '`ui_book_window TOGGLE`'


## `ui_button`

Add an on-screen button which performs a command.

USAGE: `ui_button <label> <x> <y> [-f <fontsize>] [-w <width]] [-h <height>] [-s|-l] <command>`

Add a button with specified position which will perform <command> when clicked.

-s = silent

-l = loud


## `ui_clear`

Clear all console script-generated UI elements.

USAGE: `ui_clear`


## `ui_collapsing_context_menus`

Whether right-click context menu sections can be collapsed by clicking the line above them.

USAGE: `ui_collapsing_context_menus [ON|OFF|TOGGLE]`

Displays value of `ui_collapsing_context_menus`.  If value parameter provided then sets `ui_collapsing_context_menus` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_collapsing_context_menus` = '`ui_collapsing_context_menus TOGGLE`'


## `ui_config_game_hotkeys`

Shows game-defined hotkeys config UI.

USAGE: `ui_config_game_hotkeys`

Shows the game-defined hotkeys config user interface.


## `ui_config_language`

Shows Language Selection UI.

USAGE: `ui_config_language`

Shows the language selection user interface.


## `ui_config_misc`

Shows Misc Config UI.

USAGE: `ui_config_misc`

Shows the Misc config user interface.


## `ui_config_theme`

Shows Theme Editor UI.

USAGE: `ui_config_theme`

Shows the theme editor user interface.


## `ui_config_vr`

Shows VR Config UI.

USAGE: `ui_config_vr`

Shows the VR config user interface.


## `ui_context_menus_collapsed_height`

How large the line showing the collapsed context menu section is (8-32).

USAGE: `ui_context_menus_collapsed_height [value]`

Displays value of `ui_context_menus_collapsed_height`.  If value parameter provided then sets `ui_context_menus_collapsed_height` to value specified.




## `ui_context_menus_from_games`

When ON games may create extra entries in the right-click context menus.

USAGE: `ui_context_menus_from_games [ON|OFF|TOGGLE]`

Displays value of `ui_context_menus_from_games`.  If value parameter provided then sets `ui_context_menus_from_games` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_context_menus_from_games` = '`ui_context_menus_from_games TOGGLE`'


## `ui_context_menus_show_gm_notes`

When ON and if you are Black, will display GM notes in context menu.

USAGE: `ui_context_menus_show_gm_notes [ON|OFF|TOGGLE]`

Displays value of `ui_context_menus_show_gm_notes`.  If value parameter provided then sets `ui_context_menus_show_gm_notes` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_context_menus_show_gm_notes` = '`ui_context_menus_show_gm_notes TOGGLE`'


## `ui_custom_object_check`

When ON, whenever you edit a custom object a dialog will appear if there are one or more identical custom objects which you may wish to update to match.

USAGE: `ui_custom_object_check [ON|OFF|TOGGLE]`

Displays value of `ui_custom_object_check`.  If value parameter provided then sets `ui_custom_object_check` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_custom_object_check` = '`ui_custom_object_check TOGGLE`'


## `ui_dialog_input`

Shows UIDialog:Input.

USAGE: `ui_dialog_input [<label> [<default>]]`

Shows the INPUT version of the UIDialog and then displays it's output.


## `ui_games_click`

Sends a click event to the Games dialog window.

USAGE: `ui_games_click <row> <column>`

Sends a click event to the specified button on the Games dialog window if it is currently visible.


## `ui_games_window`

The state of the Games window.  Set to ON to show it.

USAGE: `ui_games_window [ON|OFF|TOGGLE]`

Displays value of `ui_games_window`.  If value parameter provided then sets `ui_games_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_games_window` = '`ui_games_window TOGGLE`'


## `ui_gizmo_scale`

The size of the gizmo tool.

USAGE: `ui_gizmo_scale [value]`

Displays value of `ui_gizmo_scale`.  If value parameter provided then sets `ui_gizmo_scale` to value specified.




## `ui_hand_minimized_size`

Proportion of the hand view visible while minimized.

USAGE: `ui_hand_minimized_size [value]`

Displays value of `ui_hand_minimized_size`.  If value parameter provided then sets `ui_hand_minimized_size` to value specified.




## `ui_hand_view`

The on-screen hand view.

USAGE: `ui_hand_view [ON|OFF|TOGGLE]`

Displays value of `ui_hand_view`.  If value parameter provided then sets `ui_hand_view` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_hand_view` = '`ui_hand_view TOGGLE`'


## `ui_keyboard_default_state`

Whether the on-screen keyboard is shown automatically.

USAGE: `ui_keyboard_default_state <mode>`

<mode> may be one of:

 0 = Disabled

 1 = Enabled if in VR

 2 = Enabled


## `ui_keyboard_echo_duration`

How long the echo is displayed above the keyboard.  Set to 0 to turn on permanently.

USAGE: `ui_keyboard_echo_duration [value]`

Displays value of `ui_keyboard_echo_duration`.  If value parameter provided then sets `ui_keyboard_echo_duration` to value specified.




## `ui_keyboard_scale`

Size of the on-screen keyboard.

USAGE: `ui_keyboard_scale [value]`

Displays value of `ui_keyboard_scale`.  If value parameter provided then sets `ui_keyboard_scale` to value specified.




## `ui_keyboard_show`

The state of the on-screen keyboard.  Set to ON to show it.

USAGE: `ui_keyboard_show [ON|OFF|TOGGLE]`

Displays value of `ui_keyboard_show`.  If value parameter provided then sets `ui_keyboard_show` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_keyboard_show` = '`ui_keyboard_show TOGGLE`'


## `ui_label`

Add an on-screen label (non-interactive).

USAGE: `ui_label <label> <x> <y> [-f <fontsize>] [-c <color>] [-o <outline>] [-d <dropshadow>]`

Add a label at specified position.


## `ui_main_flip`

When ON the flip button on the main panel is visible.

USAGE: `ui_main_flip [ON|OFF|TOGGLE]`

Displays value of `ui_main_flip`.  If value parameter provided then sets `ui_main_flip` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_main_flip` = '`ui_main_flip TOGGLE`'


## `ui_main_modding`

When ON the modding button on the main panel is visible.

USAGE: `ui_main_modding [ON|OFF|TOGGLE]`

Displays value of `ui_main_modding`.  If value parameter provided then sets `ui_main_modding` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_main_modding` = '`ui_main_modding TOGGLE`'


## `ui_main_music`

When ON the music button on the main panel is visible.

USAGE: `ui_main_music [ON|OFF|TOGGLE]`

Displays value of `ui_main_music`.  If value parameter provided then sets `ui_main_music` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_main_music` = '`ui_main_music TOGGLE`'


## `ui_main_notebook`

When ON the notebook button on the main panel is visible.

USAGE: `ui_main_notebook [ON|OFF|TOGGLE]`

Displays value of `ui_main_notebook`.  If value parameter provided then sets `ui_main_notebook` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_main_notebook` = '`ui_main_notebook TOGGLE`'


## `ui_main_objects`

When ON the objects button on the main panel is visible.

USAGE: `ui_main_objects [ON|OFF|TOGGLE]`

Displays value of `ui_main_objects`.  If value parameter provided then sets `ui_main_objects` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_main_objects` = '`ui_main_objects TOGGLE`'


## `ui_main_options`

When ON the options button on the main panel is visible.

USAGE: `ui_main_options [ON|OFF|TOGGLE]`

Displays value of `ui_main_options`.  If value parameter provided then sets `ui_main_options` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_main_options` = '`ui_main_options TOGGLE`'


## `ui_music_player`

The state of the music player.  Set to ON to show it.

USAGE: `ui_music_player [ON|OFF|TOGGLE]`

Displays value of `ui_music_player`.  If value parameter provided then sets `ui_music_player` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_music_player` = '`ui_music_player TOGGLE`'


## `ui_objects_window`

The state of the Objects window.  Set to ON to show it.

USAGE: `ui_objects_window [ON|OFF|TOGGLE]`

Displays value of `ui_objects_window`.  If value parameter provided then sets `ui_objects_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_objects_window` = '`ui_objects_window TOGGLE`'


## `ui_panel_chat`

The state of the main panel.  Set to ON to show it.

USAGE: `ui_panel_chat [ON|OFF|TOGGLE]`

Displays value of `ui_panel_chat`.  If value parameter provided then sets `ui_panel_chat` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_panel_chat` = '`ui_panel_chat TOGGLE`'


## `ui_panel_main`

The state of the main panel.  Set to ON to show it.

USAGE: `ui_panel_main [ON|OFF|TOGGLE]`

Displays value of `ui_panel_main`.  If value parameter provided then sets `ui_panel_main` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_panel_main` = '`ui_panel_main TOGGLE`'


## `ui_panel_notepad`

The state of the player panel.  Set to ON to show it.

USAGE: `ui_panel_notepad [ON|OFF|TOGGLE]`

Displays value of `ui_panel_notepad`.  If value parameter provided then sets `ui_panel_notepad` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_panel_notepad` = '`ui_panel_notepad TOGGLE`'


## `ui_panel_player`

The state of the player panel.  Set to ON to show it.

USAGE: `ui_panel_player [ON|OFF|TOGGLE]`

Displays value of `ui_panel_player`.  If value parameter provided then sets `ui_panel_player` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_panel_player` = '`ui_panel_player TOGGLE`'


## `ui_panel_tools`

The state of tools panel.  Set to ON to show it.

USAGE: `ui_panel_tools [ON|OFF|TOGGLE]`

Displays value of `ui_panel_tools`.  If value parameter provided then sets `ui_panel_tools` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_panel_tools` = '`ui_panel_tools TOGGLE`'


## `ui_server_browser_search`

Current Server Browser search text.

USAGE: `ui_server_browser_search [value] OR ui_server_browser_search -e`

Displays value of `ui_server_browser_search`.  If value parameter provided then sets `ui_server_browser_search` to value specified.

   -e = Edit in UI editor


## `ui_server_browser_window`

The state of the server browser.  Set to ON to show it.

USAGE: `ui_server_browser_window [ON|OFF|TOGGLE]`

Displays value of `ui_server_browser_window`.  If value parameter provided then sets `ui_server_browser_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_server_browser_window` = '`ui_server_browser_window TOGGLE`'


## `ui_tag_editor_window`

The state of the tag editor window.  Set to ON to show it.

USAGE: `ui_tag_editor_window [ON|OFF|TOGGLE]`

Displays value of `ui_tag_editor_window`.  If value parameter provided then sets `ui_tag_editor_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_tag_editor_window` = '`ui_tag_editor_window TOGGLE`'


## `ui_theme_batch_end`

End a batch update of the UI Theme.

Run after ui_theme_batch_start + some ui_theme_color_ commands to refresh the UI all at once.


## `ui_theme_batch_start`

Start a batch update of the UI Theme.

When in a batch update, ui_theme_color_ commands will not refresh the UI until you run ui_theme_batch_end


## `ui_theme_color_background_tint`

The color of "Background Tint" UI elements.

USAGE: `ui_theme_color_background_tint [value] OR ui_theme_color_background_tint -e`

Displays value of `ui_theme_color_background_tint`.  If value parameter provided then sets `ui_theme_color_background_tint` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_disabled`

The color of "Button Disabled" UI elements.

USAGE: `ui_theme_color_button_disabled [value] OR ui_theme_color_button_disabled -e`

Displays value of `ui_theme_color_button_disabled`.  If value parameter provided then sets `ui_theme_color_button_disabled` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_highlight_a`

The color of "Button Highlight A" UI elements.

USAGE: `ui_theme_color_button_highlight_a [value] OR ui_theme_color_button_highlight_a -e`

Displays value of `ui_theme_color_button_highlight_a`.  If value parameter provided then sets `ui_theme_color_button_highlight_a` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_highlight_b`

The color of "Button Highlight B" UI elements.

USAGE: `ui_theme_color_button_highlight_b [value] OR ui_theme_color_button_highlight_b -e`

Displays value of `ui_theme_color_button_highlight_b`.  If value parameter provided then sets `ui_theme_color_button_highlight_b` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_highlight_c`

The color of "Button Highlight C" UI elements.

USAGE: `ui_theme_color_button_highlight_c [value] OR ui_theme_color_button_highlight_c -e`

Displays value of `ui_theme_color_button_highlight_c`.  If value parameter provided then sets `ui_theme_color_button_highlight_c` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_hover`

The color of "Button Hover" UI elements.

USAGE: `ui_theme_color_button_hover [value] OR ui_theme_color_button_hover -e`

Displays value of `ui_theme_color_button_hover`.  If value parameter provided then sets `ui_theme_color_button_hover` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_neutral`

The color of "Button Neutral" UI elements.

USAGE: `ui_theme_color_button_neutral [value] OR ui_theme_color_button_neutral -e`

Displays value of `ui_theme_color_button_neutral`.  If value parameter provided then sets `ui_theme_color_button_neutral` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_normal`

The color of "Button Normal" UI elements.

USAGE: `ui_theme_color_button_normal [value] OR ui_theme_color_button_normal -e`

Displays value of `ui_theme_color_button_normal`.  If value parameter provided then sets `ui_theme_color_button_normal` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_button_pressed`

The color of "Button Pressed" UI elements.

USAGE: `ui_theme_color_button_pressed [value] OR ui_theme_color_button_pressed -e`

Displays value of `ui_theme_color_button_pressed`.  If value parameter provided then sets `ui_theme_color_button_pressed` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_caret`

The color of "Caret" UI elements.

USAGE: `ui_theme_color_caret [value] OR ui_theme_color_caret -e`

Displays value of `ui_theme_color_caret`.  If value parameter provided then sets `ui_theme_color_caret` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_input_background`

The color of "Chat Input Background" UI elements.

USAGE: `ui_theme_color_chat_input_background [value] OR ui_theme_color_chat_input_background -e`

Displays value of `ui_theme_color_chat_input_background`.  If value parameter provided then sets `ui_theme_color_chat_input_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_input_controls`

The color of "Chat Input Controls" UI elements.

USAGE: `ui_theme_color_chat_input_controls [value] OR ui_theme_color_chat_input_controls -e`

Displays value of `ui_theme_color_chat_input_controls`.  If value parameter provided then sets `ui_theme_color_chat_input_controls` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_input_text`

The color of "Chat Input Text" UI elements.

USAGE: `ui_theme_color_chat_input_text [value] OR ui_theme_color_chat_input_text -e`

Displays value of `ui_theme_color_chat_input_text`.  If value parameter provided then sets `ui_theme_color_chat_input_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_output_background`

The color of "Chat Output Background" UI elements.

USAGE: `ui_theme_color_chat_output_background [value] OR ui_theme_color_chat_output_background -e`

Displays value of `ui_theme_color_chat_output_background`.  If value parameter provided then sets `ui_theme_color_chat_output_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_output_controls`

The color of "Chat Output Controls" UI elements.

USAGE: `ui_theme_color_chat_output_controls [value] OR ui_theme_color_chat_output_controls -e`

Displays value of `ui_theme_color_chat_output_controls`.  If value parameter provided then sets `ui_theme_color_chat_output_controls` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_tab_background`

The color of "Chat Tab Background" UI elements.

USAGE: `ui_theme_color_chat_tab_background [value] OR ui_theme_color_chat_tab_background -e`

Displays value of `ui_theme_color_chat_tab_background`.  If value parameter provided then sets `ui_theme_color_chat_tab_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_chat_tab_highlight`

The color of "Chat Tab Highlight" UI elements.

USAGE: `ui_theme_color_chat_tab_highlight [value] OR ui_theme_color_chat_tab_highlight -e`

Displays value of `ui_theme_color_chat_tab_highlight`.  If value parameter provided then sets `ui_theme_color_chat_tab_highlight` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_check_box_background`

The color of "Check Box Background" UI elements.

USAGE: `ui_theme_color_check_box_background [value] OR ui_theme_color_check_box_background -e`

Displays value of `ui_theme_color_check_box_background`.  If value parameter provided then sets `ui_theme_color_check_box_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_check_box_pressed`

The color of "Check Box Pressed" UI elements.

USAGE: `ui_theme_color_check_box_pressed [value] OR ui_theme_color_check_box_pressed -e`

Displays value of `ui_theme_color_check_box_pressed`.  If value parameter provided then sets `ui_theme_color_check_box_pressed` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_console_input_background`

The color of "Console Input Background" UI elements.

USAGE: `ui_theme_color_console_input_background [value] OR ui_theme_color_console_input_background -e`

Displays value of `ui_theme_color_console_input_background`.  If value parameter provided then sets `ui_theme_color_console_input_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_console_input_controls`

The color of "Console Input Controls" UI elements.

USAGE: `ui_theme_color_console_input_controls [value] OR ui_theme_color_console_input_controls -e`

Displays value of `ui_theme_color_console_input_controls`.  If value parameter provided then sets `ui_theme_color_console_input_controls` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_console_input_text`

The color of "Console Input Text" UI elements.

USAGE: `ui_theme_color_console_input_text [value] OR ui_theme_color_console_input_text -e`

Displays value of `ui_theme_color_console_input_text`.  If value parameter provided then sets `ui_theme_color_console_input_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_console_output_background`

The color of "Console Output Background" UI elements.

USAGE: `ui_theme_color_console_output_background [value] OR ui_theme_color_console_output_background -e`

Displays value of `ui_theme_color_console_output_background`.  If value parameter provided then sets `ui_theme_color_console_output_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_console_output_controls`

The color of "Console Output Controls" UI elements.

USAGE: `ui_theme_color_console_output_controls [value] OR ui_theme_color_console_output_controls -e`

Displays value of `ui_theme_color_console_output_controls`.  If value parameter provided then sets `ui_theme_color_console_output_controls` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_context_menu_background`

The color of "Context Menu Background" UI elements.

USAGE: `ui_theme_color_context_menu_background [value] OR ui_theme_color_context_menu_background -e`

Displays value of `ui_theme_color_context_menu_background`.  If value parameter provided then sets `ui_theme_color_context_menu_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_context_menu_highlight`

The color of "Context Menu Highlight" UI elements.

USAGE: `ui_theme_color_context_menu_highlight [value] OR ui_theme_color_context_menu_highlight -e`

Displays value of `ui_theme_color_context_menu_highlight`.  If value parameter provided then sets `ui_theme_color_context_menu_highlight` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_context_menu_hover`

The color of "Context Menu Hover" UI elements.

USAGE: `ui_theme_color_context_menu_hover [value] OR ui_theme_color_context_menu_hover -e`

Displays value of `ui_theme_color_context_menu_hover`.  If value parameter provided then sets `ui_theme_color_context_menu_hover` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_context_menu_text`

The color of "Context Menu Text" UI elements.

USAGE: `ui_theme_color_context_menu_text [value] OR ui_theme_color_context_menu_text -e`

Displays value of `ui_theme_color_context_menu_text`.  If value parameter provided then sets `ui_theme_color_context_menu_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_control_background`

The color of "Control Background" UI elements.

USAGE: `ui_theme_color_control_background [value] OR ui_theme_color_control_background -e`

Displays value of `ui_theme_color_control_background`.  If value parameter provided then sets `ui_theme_color_control_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_divider`

The color of "Divider" UI elements.

USAGE: `ui_theme_color_divider [value] OR ui_theme_color_divider -e`

Displays value of `ui_theme_color_divider`.  If value parameter provided then sets `ui_theme_color_divider` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_floating_text`

The color of "Floating Text" UI elements.

USAGE: `ui_theme_color_floating_text [value] OR ui_theme_color_floating_text -e`

Displays value of `ui_theme_color_floating_text`.  If value parameter provided then sets `ui_theme_color_floating_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_glow`

The color of "Glow" UI elements.

USAGE: `ui_theme_color_glow [value] OR ui_theme_color_glow -e`

Displays value of `ui_theme_color_glow`.  If value parameter provided then sets `ui_theme_color_glow` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_high`

The color of "High" UI elements.

USAGE: `ui_theme_color_high [value] OR ui_theme_color_high -e`

Displays value of `ui_theme_color_high`.  If value parameter provided then sets `ui_theme_color_high` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_hover_highlight`

The color of "Hover Highlight" UI elements.

USAGE: `ui_theme_color_hover_highlight [value] OR ui_theme_color_hover_highlight -e`

Displays value of `ui_theme_color_hover_highlight`.  If value parameter provided then sets `ui_theme_color_hover_highlight` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_input_text_active`

The color of "Input Text Active" UI elements.

USAGE: `ui_theme_color_input_text_active [value] OR ui_theme_color_input_text_active -e`

Displays value of `ui_theme_color_input_text_active`.  If value parameter provided then sets `ui_theme_color_input_text_active` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_input_text_inactive`

The color of "Input Text Inactive" UI elements.

USAGE: `ui_theme_color_input_text_inactive [value] OR ui_theme_color_input_text_inactive -e`

Displays value of `ui_theme_color_input_text_inactive`.  If value parameter provided then sets `ui_theme_color_input_text_inactive` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_label`

The color of "Label" UI elements.

USAGE: `ui_theme_color_label [value] OR ui_theme_color_label -e`

Displays value of `ui_theme_color_label`.  If value parameter provided then sets `ui_theme_color_label` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_low`

The color of "Low" UI elements.

USAGE: `ui_theme_color_low [value] OR ui_theme_color_low -e`

Displays value of `ui_theme_color_low`.  If value parameter provided then sets `ui_theme_color_low` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_lua_background`

The color of "Lua Background" UI elements.

USAGE: `ui_theme_color_lua_background [value] OR ui_theme_color_lua_background -e`

Displays value of `ui_theme_color_lua_background`.  If value parameter provided then sets `ui_theme_color_lua_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_lua_caret`

The color of "Lua Caret" UI elements.

USAGE: `ui_theme_color_lua_caret [value] OR ui_theme_color_lua_caret -e`

Displays value of `ui_theme_color_lua_caret`.  If value parameter provided then sets `ui_theme_color_lua_caret` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_lua_selection`

The color of "Lua Selection" UI elements.

USAGE: `ui_theme_color_lua_selection [value] OR ui_theme_color_lua_selection -e`

Displays value of `ui_theme_color_lua_selection`.  If value parameter provided then sets `ui_theme_color_lua_selection` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_lua_text`

The color of "Lua Text" UI elements.

USAGE: `ui_theme_color_lua_text [value] OR ui_theme_color_lua_text -e`

Displays value of `ui_theme_color_lua_text`.  If value parameter provided then sets `ui_theme_color_lua_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_measurement_inner`

The color of "Measurement Inner" UI elements.

USAGE: `ui_theme_color_measurement_inner [value] OR ui_theme_color_measurement_inner -e`

Displays value of `ui_theme_color_measurement_inner`.  If value parameter provided then sets `ui_theme_color_measurement_inner` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_measurement_outer`

The color of "Measurement Outer" UI elements.

USAGE: `ui_theme_color_measurement_outer [value] OR ui_theme_color_measurement_outer -e`

Displays value of `ui_theme_color_measurement_outer`.  If value parameter provided then sets `ui_theme_color_measurement_outer` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_motif`

The color of "Motif" UI elements.

USAGE: `ui_theme_color_motif [value] OR ui_theme_color_motif -e`

Displays value of `ui_theme_color_motif`.  If value parameter provided then sets `ui_theme_color_motif` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_motif_highlight_a`

The color of "Motif Highlight A" UI elements.

USAGE: `ui_theme_color_motif_highlight_a [value] OR ui_theme_color_motif_highlight_a -e`

Displays value of `ui_theme_color_motif_highlight_a`.  If value parameter provided then sets `ui_theme_color_motif_highlight_a` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_motif_highlight_b`

The color of "Motif Highlight B" UI elements.

USAGE: `ui_theme_color_motif_highlight_b [value] OR ui_theme_color_motif_highlight_b -e`

Displays value of `ui_theme_color_motif_highlight_b`.  If value parameter provided then sets `ui_theme_color_motif_highlight_b` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_note_edit_text`

The color of "Note Edit Text" UI elements.

USAGE: `ui_theme_color_note_edit_text [value] OR ui_theme_color_note_edit_text -e`

Displays value of `ui_theme_color_note_edit_text`.  If value parameter provided then sets `ui_theme_color_note_edit_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_black`

The color of "Player Black" UI elements.

USAGE: `ui_theme_color_player_black [value] OR ui_theme_color_player_black -e`

Displays value of `ui_theme_color_player_black`.  If value parameter provided then sets `ui_theme_color_player_black` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_blue`

The color of "Player Blue" UI elements.

USAGE: `ui_theme_color_player_blue [value] OR ui_theme_color_player_blue -e`

Displays value of `ui_theme_color_player_blue`.  If value parameter provided then sets `ui_theme_color_player_blue` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_brown`

The color of "Player Brown" UI elements.

USAGE: `ui_theme_color_player_brown [value] OR ui_theme_color_player_brown -e`

Displays value of `ui_theme_color_player_brown`.  If value parameter provided then sets `ui_theme_color_player_brown` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_green`

The color of "Player Green" UI elements.

USAGE: `ui_theme_color_player_green [value] OR ui_theme_color_player_green -e`

Displays value of `ui_theme_color_player_green`.  If value parameter provided then sets `ui_theme_color_player_green` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_grey`

The color of "Player Grey" UI elements.

USAGE: `ui_theme_color_player_grey [value] OR ui_theme_color_player_grey -e`

Displays value of `ui_theme_color_player_grey`.  If value parameter provided then sets `ui_theme_color_player_grey` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_orange`

The color of "Player Orange" UI elements.

USAGE: `ui_theme_color_player_orange [value] OR ui_theme_color_player_orange -e`

Displays value of `ui_theme_color_player_orange`.  If value parameter provided then sets `ui_theme_color_player_orange` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_pink`

The color of "Player Pink" UI elements.

USAGE: `ui_theme_color_player_pink [value] OR ui_theme_color_player_pink -e`

Displays value of `ui_theme_color_player_pink`.  If value parameter provided then sets `ui_theme_color_player_pink` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_purple`

The color of "Player Purple" UI elements.

USAGE: `ui_theme_color_player_purple [value] OR ui_theme_color_player_purple -e`

Displays value of `ui_theme_color_player_purple`.  If value parameter provided then sets `ui_theme_color_player_purple` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_red`

The color of "Player Red" UI elements.

USAGE: `ui_theme_color_player_red [value] OR ui_theme_color_player_red -e`

Displays value of `ui_theme_color_player_red`.  If value parameter provided then sets `ui_theme_color_player_red` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_teal`

The color of "Player Teal" UI elements.

USAGE: `ui_theme_color_player_teal [value] OR ui_theme_color_player_teal -e`

Displays value of `ui_theme_color_player_teal`.  If value parameter provided then sets `ui_theme_color_player_teal` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_white`

The color of "Player White" UI elements.

USAGE: `ui_theme_color_player_white [value] OR ui_theme_color_player_white -e`

Displays value of `ui_theme_color_player_white`.  If value parameter provided then sets `ui_theme_color_player_white` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_player_yellow`

The color of "Player Yellow" UI elements.

USAGE: `ui_theme_color_player_yellow [value] OR ui_theme_color_player_yellow -e`

Displays value of `ui_theme_color_player_yellow`.  If value parameter provided then sets `ui_theme_color_player_yellow` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_sky_above`

The color of "Pure Sky Above" UI elements.

USAGE: `ui_theme_color_pure_sky_above [value] OR ui_theme_color_pure_sky_above -e`

Displays value of `ui_theme_color_pure_sky_above`.  If value parameter provided then sets `ui_theme_color_pure_sky_above` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_sky_below`

The color of "Pure Sky Below" UI elements.

USAGE: `ui_theme_color_pure_sky_below [value] OR ui_theme_color_pure_sky_below -e`

Displays value of `ui_theme_color_pure_sky_below`.  If value parameter provided then sets `ui_theme_color_pure_sky_below` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_sky_horizon`

The color of "Pure Sky Horizon" UI elements.

USAGE: `ui_theme_color_pure_sky_horizon [value] OR ui_theme_color_pure_sky_horizon -e`

Displays value of `ui_theme_color_pure_sky_horizon`.  If value parameter provided then sets `ui_theme_color_pure_sky_horizon` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_splash`

The color of "Pure Splash" UI elements.

USAGE: `ui_theme_color_pure_splash [value] OR ui_theme_color_pure_splash -e`

Displays value of `ui_theme_color_pure_splash`.  If value parameter provided then sets `ui_theme_color_pure_splash` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_splash_specular`

The color of "Pure Splash Specular" UI elements.

USAGE: `ui_theme_color_pure_splash_specular [value] OR ui_theme_color_pure_splash_specular -e`

Displays value of `ui_theme_color_pure_splash_specular`.  If value parameter provided then sets `ui_theme_color_pure_splash_specular` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_table_a`

The color of "Pure Table A" UI elements.

USAGE: `ui_theme_color_pure_table_a [value] OR ui_theme_color_pure_table_a -e`

Displays value of `ui_theme_color_pure_table_a`.  If value parameter provided then sets `ui_theme_color_pure_table_a` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_table_a_specular`

The color of "Pure Table A Specular" UI elements.

USAGE: `ui_theme_color_pure_table_a_specular [value] OR ui_theme_color_pure_table_a_specular -e`

Displays value of `ui_theme_color_pure_table_a_specular`.  If value parameter provided then sets `ui_theme_color_pure_table_a_specular` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_table_b`

The color of "Pure Table B" UI elements.

USAGE: `ui_theme_color_pure_table_b [value] OR ui_theme_color_pure_table_b -e`

Displays value of `ui_theme_color_pure_table_b`.  If value parameter provided then sets `ui_theme_color_pure_table_b` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_pure_table_b_specular`

The color of "Pure Table B Specular" UI elements.

USAGE: `ui_theme_color_pure_table_b_specular [value] OR ui_theme_color_pure_table_b_specular -e`

Displays value of `ui_theme_color_pure_table_b_specular`.  If value parameter provided then sets `ui_theme_color_pure_table_b_specular` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_radio_button_background`

The color of "Radio Button Background" UI elements.

USAGE: `ui_theme_color_radio_button_background [value] OR ui_theme_color_radio_button_background -e`

Displays value of `ui_theme_color_radio_button_background`.  If value parameter provided then sets `ui_theme_color_radio_button_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_radio_button_pressed`

The color of "Radio Button Pressed" UI elements.

USAGE: `ui_theme_color_radio_button_pressed [value] OR ui_theme_color_radio_button_pressed -e`

Displays value of `ui_theme_color_radio_button_pressed`.  If value parameter provided then sets `ui_theme_color_radio_button_pressed` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_selection`

The color of "Selection" UI elements.

USAGE: `ui_theme_color_selection [value] OR ui_theme_color_selection -e`

Displays value of `ui_theme_color_selection`.  If value parameter provided then sets `ui_theme_color_selection` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_slider_label`

The color of "Slider Label" UI elements.

USAGE: `ui_theme_color_slider_label [value] OR ui_theme_color_slider_label -e`

Displays value of `ui_theme_color_slider_label`.  If value parameter provided then sets `ui_theme_color_slider_label` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_slider_normal`

The color of "Slider Normal" UI elements.

USAGE: `ui_theme_color_slider_normal [value] OR ui_theme_color_slider_normal -e`

Displays value of `ui_theme_color_slider_normal`.  If value parameter provided then sets `ui_theme_color_slider_normal` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_slider_pressed`

The color of "Slider Pressed" UI elements.

USAGE: `ui_theme_color_slider_pressed [value] OR ui_theme_color_slider_pressed -e`

Displays value of `ui_theme_color_slider_pressed`.  If value parameter provided then sets `ui_theme_color_slider_pressed` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_splash`

The color of "Splash" UI elements.

USAGE: `ui_theme_color_splash [value] OR ui_theme_color_splash -e`

Displays value of `ui_theme_color_splash`.  If value parameter provided then sets `ui_theme_color_splash` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_splash_highlight`

The color of "Splash Highlight" UI elements.

USAGE: `ui_theme_color_splash_highlight [value] OR ui_theme_color_splash_highlight -e`

Displays value of `ui_theme_color_splash_highlight`.  If value parameter provided then sets `ui_theme_color_splash_highlight` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tab_active`

The color of "Tab Active" UI elements.

USAGE: `ui_theme_color_tab_active [value] OR ui_theme_color_tab_active -e`

Displays value of `ui_theme_color_tab_active`.  If value parameter provided then sets `ui_theme_color_tab_active` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tab_normal`

The color of "Tab Normal" UI elements.

USAGE: `ui_theme_color_tab_normal [value] OR ui_theme_color_tab_normal -e`

Displays value of `ui_theme_color_tab_normal`.  If value parameter provided then sets `ui_theme_color_tab_normal` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tab_strip`

The color of "Tab Strip" UI elements.

USAGE: `ui_theme_color_tab_strip [value] OR ui_theme_color_tab_strip -e`

Displays value of `ui_theme_color_tab_strip`.  If value parameter provided then sets `ui_theme_color_tab_strip` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tooltip_background`

The color of "Tooltip Background" UI elements.

USAGE: `ui_theme_color_tooltip_background [value] OR ui_theme_color_tooltip_background -e`

Displays value of `ui_theme_color_tooltip_background`.  If value parameter provided then sets `ui_theme_color_tooltip_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tooltip_border`

The color of "Tooltip Border" UI elements.

USAGE: `ui_theme_color_tooltip_border [value] OR ui_theme_color_tooltip_border -e`

Displays value of `ui_theme_color_tooltip_border`.  If value parameter provided then sets `ui_theme_color_tooltip_border` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tooltip_motif`

The color of "Tooltip Motif" UI elements.

USAGE: `ui_theme_color_tooltip_motif [value] OR ui_theme_color_tooltip_motif -e`

Displays value of `ui_theme_color_tooltip_motif`.  If value parameter provided then sets `ui_theme_color_tooltip_motif` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_tooltip_text`

The color of "Tooltip Text" UI elements.

USAGE: `ui_theme_color_tooltip_text [value] OR ui_theme_color_tooltip_text -e`

Displays value of `ui_theme_color_tooltip_text`.  If value parameter provided then sets `ui_theme_color_tooltip_text` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_transparent_background`

The color of "Transparent Background" UI elements.

USAGE: `ui_theme_color_transparent_background [value] OR ui_theme_color_transparent_background -e`

Displays value of `ui_theme_color_transparent_background`.  If value parameter provided then sets `ui_theme_color_transparent_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_color_window_background`

The color of "Window Background" UI elements.

USAGE: `ui_theme_color_window_background [value] OR ui_theme_color_window_background -e`

Displays value of `ui_theme_color_window_background`.  If value parameter provided then sets `ui_theme_color_window_background` to value specified.

   -e = Edit in UI editor


## `ui_theme_count`

Number of currently available UI themes.

USAGE: `ui_theme_count [value]`

Displays value of `ui_theme_count`.  If value parameter provided then sets `ui_theme_count` to value specified.




## `ui_theme_from_game_auto`

When ON games you join or load may set the theme colours for you.

USAGE: `ui_theme_from_game_auto [ON|OFF|TOGGLE]`

Displays value of `ui_theme_from_game_auto`.  If value parameter provided then sets `ui_theme_from_game_auto` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_theme_from_game_auto` = '`ui_theme_from_game_auto TOGGLE`'


## `ui_theme_index`

Index of currently selected UI theme.

USAGE: `ui_theme_index [value]`

Displays value of `ui_theme_index`.  If value parameter provided then sets `ui_theme_index` to value specified.




## `ui_theme_is_dark`

Activate Dark Theme

Activate Dark Theme


## `ui_theme_is_from_game`

Set theme to the one provided by the current game

USAGE: `ui_theme_is_from_game`


## `ui_theme_is_light`

Activate Light Theme

Activate Light Theme


## `ui_theme_is_mine`

Activate Mine Theme

Activate Mine Theme


## `ui_theme_minimum_opacity`

When ui_theme_restrict_transparency is ON this set the minimum value of alpha.

USAGE: `ui_theme_minimum_opacity [value]`

Displays value of `ui_theme_minimum_opacity`.  If value parameter provided then sets `ui_theme_minimum_opacity` to value specified.




## `ui_theme_name`

Name of currently selected UI theme.  
Setting will load the specified theme, if it exists (unless currently within a batch theme update).

USAGE: `ui_theme_name [value] OR ui_theme_name -e`

Displays value of `ui_theme_name`.  If value parameter provided then sets `ui_theme_name` to value specified.

   -e = Edit in UI editor


## `ui_theme_restrict_transparency`

When ON the alpha value of colours will always be at least 50%

USAGE: `ui_theme_restrict_transparency [ON|OFF|TOGGLE]`

Displays value of `ui_theme_restrict_transparency`.  If value parameter provided then sets `ui_theme_restrict_transparency` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_theme_restrict_transparency` = '`ui_theme_restrict_transparency TOGGLE`'


## `ui_toggle`

Add an on-screen checkbox attached to a toggle variable.

USAGE: `ui_toggle <label> <x> <y> [-r] [-f <fontsize>] [-c <color>] [-o <outline>] [-d <dropshadow>] [-w <width>] [-s|-l] <variable>`

Add a checkbox with specified position which will be attatched to <variable>.

-r = label on right

-s = silent

-l = loud

<outline> and <dropshadow> specify color.


## `ui_tooltip_delay`

Length of time you must hover over a UI element before the verbose tooltip is displayed.

USAGE: `ui_tooltip_delay [value]`

Displays value of `ui_tooltip_delay`.  If value parameter provided then sets `ui_tooltip_delay` to value specified.




## `ui_tooltip_indicator`

When ON tooltips are indicated with a (?) postfix.

USAGE: `ui_tooltip_indicator [ON|OFF|TOGGLE]`

Displays value of `ui_tooltip_indicator`.  If value parameter provided then sets `ui_tooltip_indicator` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_tooltip_indicator` = '`ui_tooltip_indicator TOGGLE`'


## `ui_visualize_drop_free`

Display drop location indicator when holding object which are not going to snap to a point.

USAGE: `ui_visualize_drop_free [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_drop_free`.  If value parameter provided then sets `ui_visualize_drop_free` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_drop_free` = '`ui_visualize_drop_free TOGGLE`'


## `ui_visualize_drop_grid`

Display drop location indicator when holding object which will snap to a grid point.

USAGE: `ui_visualize_drop_grid [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_drop_grid`.  If value parameter provided then sets `ui_visualize_drop_grid` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_drop_grid` = '`ui_visualize_drop_grid TOGGLE`'


## `ui_visualize_drop_opacity`

Opacity of drop location indicator.

USAGE: `ui_visualize_drop_opacity [value]`

Displays value of `ui_visualize_drop_opacity`.  If value parameter provided then sets `ui_visualize_drop_opacity` to value specified.




## `ui_visualize_drop_snap`

Display drop location indicator when holding object which will snap to a snap point.

USAGE: `ui_visualize_drop_snap [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_drop_snap`.  If value parameter provided then sets `ui_visualize_drop_snap` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_drop_snap` = '`ui_visualize_drop_snap TOGGLE`'


## `ui_visualize_drops`

Enable/disable drop location indicators.

USAGE: `ui_visualize_drops [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_drops`.  If value parameter provided then sets `ui_visualize_drops` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_drops` = '`ui_visualize_drops TOGGLE`'


## `ui_visualize_spawn_hide_window`

Hide components window while spawning objects.

USAGE: `ui_visualize_spawn_hide_window [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_spawn_hide_window`.  If value parameter provided then sets `ui_visualize_spawn_hide_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_spawn_hide_window` = '`ui_visualize_spawn_hide_window TOGGLE`'


## `ui_visualize_spawn_in_air`

When ON objects will spawn above the table instead of directly on the table. Holding <CTRL> flips this behaviour.

USAGE: `ui_visualize_spawn_in_air [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_spawn_in_air`.  If value parameter provided then sets `ui_visualize_spawn_in_air` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_spawn_in_air` = '`ui_visualize_spawn_in_air TOGGLE`'


## `ui_visualize_spawn_object_snap`

When spawning objects while hovering over an object, do they snap to it.

USAGE: `ui_visualize_spawn_object_snap [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_spawn_object_snap`.  If value parameter provided then sets `ui_visualize_spawn_object_snap` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_spawn_object_snap` = '`ui_visualize_spawn_object_snap TOGGLE`'


## `ui_visualize_spawn_opacity`

Opacity of spawn location indicator.

USAGE: `ui_visualize_spawn_opacity [value]`

Displays value of `ui_visualize_spawn_opacity`.  If value parameter provided then sets `ui_visualize_spawn_opacity` to value specified.




## `ui_visualize_spawn_right_click_ends`

Exit Spawn mode by hitting right-click.

USAGE: `ui_visualize_spawn_right_click_ends [ON|OFF|TOGGLE]`

Displays value of `ui_visualize_spawn_right_click_ends`.  If value parameter provided then sets `ui_visualize_spawn_right_click_ends` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!ui_visualize_spawn_right_click_ends` = '`ui_visualize_spawn_right_click_ends TOGGLE`'


## `unbind`

Unbinds a key.

USAGE: `unbind [-a] <key>`

Removes any command bound to <key>. If '-a' specified then unbinds all versions of <key> (+-!).


## `unload_interval`

Time in seconds between each unload (cleanup the game can cause stutter).  If set to 0 then unload timer is disabled.

USAGE: `unload_interval [value]`

Displays value of `unload_interval`.  If value parameter provided then sets `unload_interval` to value specified.




## `variables`

Lists all variables and their values.

USAGE: `variables <prefix>`

Displays all available commands which are variables and what they are currently set to.

If prefix is supplied then only commands which start with it will be displayed.


## `vector_x`

Get the X component of a vector variable.

USAGE: `vector_x [<variable>]`

If <variable> specified then set vector_x to be its X component.


## `vector_y`

Get the Y component of a vector variable.

USAGE: `vector_y [<variable>]`

If <variable> specified then set vector_y to be its Y component.


## `vector_z`

Get the Z component of a vector variable.

USAGE: `vector_z [<variable>]`

If <variable> specified then set vector_z to be its Z component.


## `version`

Displays version information.

USAGE: `version`

Displays information on current game version.


## `vr_active`

Is VR currently active?

Reports whether game is currently running in VR mode (READ ONLY).


## `vr_controller_alpha_body`

Sets the opacity of the VR controllers: 0.0 = transparent, 1.0 = opaque.

USAGE: `vr_controller_alpha_body [value]`

Displays value of `vr_controller_alpha_body`.  If value parameter provided then sets `vr_controller_alpha_body` to value specified.




## `vr_controller_alpha_gem`

Sets the opacity of the VR controller gem: 0.0 = transparent, 1.0 = opaque.

USAGE: `vr_controller_alpha_gem [value]`

Displays value of `vr_controller_alpha_gem`.  If value parameter provided then sets `vr_controller_alpha_gem` to value specified.




## `vr_controller_alpha_icons`

Sets the opacity of the VR controller icons: 0.0 = transparent, 1.0 = opaque.

USAGE: `vr_controller_alpha_icons [value]`

Displays value of `vr_controller_alpha_icons`.  If value parameter provided then sets `vr_controller_alpha_icons` to value specified.




## `vr_controls_original`

If ON then controllers use the original control scheme.

USAGE: `vr_controls_original [ON|OFF|TOGGLE]`

Displays value of `vr_controls_original`.  If value parameter provided then sets `vr_controls_original` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_controls_original` = '`vr_controls_original TOGGLE`'


## `vr_display_network_players_all`

Display controllers and headsets for other VR players.

USAGE: `vr_display_network_players_all`


## `vr_display_network_players_hands`

Display controllers for other VR players.

USAGE: `vr_display_network_players_hands`


## `vr_display_network_players_off`

Turn off displaying other VR players.

USAGE: `vr_display_network_players_off`


## `vr_grabbing_hides_gem`

If ON then the interaction gem will be hidden when you grab an object..

USAGE: `vr_grabbing_hides_gem [ON|OFF|TOGGLE]`

Displays value of `vr_grabbing_hides_gem`.  If value parameter provided then sets `vr_grabbing_hides_gem` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_grabbing_hides_gem` = '`vr_grabbing_hides_gem TOGGLE`'


## `vr_hand_view_angle`

The angle the hand view is offset from the controller.

USAGE: `vr_hand_view_angle [value]`

Displays value of `vr_hand_view_angle`.  If value parameter provided then sets `vr_hand_view_angle` to value specified.




## `vr_hand_view_detach`

Detach (turn off) the virtual hand view.

USAGE: `vr_hand_view_detach`


## `vr_hand_view_hide_on_grab`

If ON then the virtual hand will be hidden when its controller is used to grab something.

USAGE: `vr_hand_view_hide_on_grab [ON|OFF|TOGGLE]`

Displays value of `vr_hand_view_hide_on_grab`.  If value parameter provided then sets `vr_hand_view_hide_on_grab` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_hand_view_hide_on_grab` = '`vr_hand_view_hide_on_grab TOGGLE`'


## `vr_hand_view_scale`

Scale applied to virtual hand. Must be > 0.

USAGE: `vr_hand_view_scale [value]`

Displays value of `vr_hand_view_scale`.  If value parameter provided then sets `vr_hand_view_scale` to value specified.




## `vr_haptic_test`

Triggers the haptic feedback on the VR controllers.

USAGE: `vr_haptic_test [<intensity>]`


## `vr_hover_tooltips`

When ON tooltips displayed when hovering over UI items will be displayed above the touchpad icons.

USAGE: `vr_hover_tooltips [ON|OFF|TOGGLE]`

Displays value of `vr_hover_tooltips`.  If value parameter provided then sets `vr_hover_tooltips` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_hover_tooltips` = '`vr_hover_tooltips TOGGLE`'


## `vr_interface_click_threshold`

When interface click is bound to an analog input it obeys this threshold.

USAGE: `vr_interface_click_threshold [value]`

Displays value of `vr_interface_click_threshold`.  If value parameter provided then sets `vr_interface_click_threshold` to value specified.




## `vr_interface_repeat_duration`

Sets how long you have to hold a button for it to repeat a repeatable action.

USAGE: `vr_interface_repeat_duration [value]`

Displays value of `vr_interface_repeat_duration`.  If value parameter provided then sets `vr_interface_repeat_duration` to value specified.




## `vr_joypad_emulation`

If ON then joypad bindings on VR controllers will be enabled, allowing you to use them for in-game actions.

USAGE: `vr_joypad_emulation [ON|OFF|TOGGLE]`

Displays value of `vr_joypad_emulation`.  If value parameter provided then sets `vr_joypad_emulation` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_joypad_emulation` = '`vr_joypad_emulation TOGGLE`'


## `vr_laser_activation_threshold`

When laser activation is bound to an analog input it obeys this threshold.

USAGE: `vr_laser_activation_threshold [value]`

Displays value of `vr_laser_activation_threshold`.  If value parameter provided then sets `vr_laser_activation_threshold` to value specified.




## `vr_laser_angled`

If ON then controller laser pointer will always be angled like under original controls.

USAGE: `vr_laser_angled [ON|OFF|TOGGLE]`

Displays value of `vr_laser_angled`.  If value parameter provided then sets `vr_laser_angled` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_laser_angled` = '`vr_laser_angled TOGGLE`'


## `vr_laser_beam_opacity`

Sets opacity of the laser beam: 0.0 = transparent, 1.0 = opaque.

USAGE: `vr_laser_beam_opacity [value]`

Displays value of `vr_laser_beam_opacity`.  If value parameter provided then sets `vr_laser_beam_opacity` to value specified.




## `vr_laser_beam_thickness`

Sets how thick the laser beam is.

USAGE: `vr_laser_beam_thickness [value]`

Displays value of `vr_laser_beam_thickness`.  If value parameter provided then sets `vr_laser_beam_thickness` to value specified.




## `vr_laser_beam_visible`

If ON then controller laser pointer beam will be visible. Laser dot is always visible when laser is on.

USAGE: `vr_laser_beam_visible [ON|OFF|TOGGLE]`

Displays value of `vr_laser_beam_visible`.  If value parameter provided then sets `vr_laser_beam_visible` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_laser_beam_visible` = '`vr_laser_beam_visible TOGGLE`'


## `vr_laser_constant`

If ON then controller laser pointer will always be on like under original controls.

USAGE: `vr_laser_constant [ON|OFF|TOGGLE]`

Displays value of `vr_laser_constant`.  If value parameter provided then sets `vr_laser_constant` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_laser_constant` = '`vr_laser_constant TOGGLE`'


## `vr_laser_dot_size`

Sets how large the laser hit dot is.

USAGE: `vr_laser_dot_size [value]`

Displays value of `vr_laser_dot_size`.  If value parameter provided then sets `vr_laser_dot_size` to value specified.




## `vr_left_controller_attach_hand_view`

Attached the virtual hand view to the left controller.

USAGE: `vr_left_controller_attach_hand_view`


## `vr_left_controller_bind_tool_hotkeys`

When ON the left controller's default tool selection hotkeys will be bound to its pad.

USAGE: `vr_left_controller_bind_tool_hotkeys [ON|OFF|TOGGLE]`

Displays value of `vr_left_controller_bind_tool_hotkeys`.  If value parameter provided then sets `vr_left_controller_bind_tool_hotkeys` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_left_controller_bind_tool_hotkeys` = '`vr_left_controller_bind_tool_hotkeys TOGGLE`'


## `vr_left_controller_mode_pad_down`

Controls whether pad down on the left controller is bindable, displays the tool selecter, or zooms the active object.

USAGE: `vr_left_controller_mode_pad_down <mode>`

<mode> may be one of:

 0 = Bindable

 1 = Tool Select

 2 = Zoom


## `vr_left_controller_pad_down_bindable`

Sets the left controller pad down mode to Bindable.

USAGE: `vr_left_controller_pad_down_bindable`


## `vr_left_controller_pad_down_tool_select`

Sets the left controller pad down mode to Tool Select.

USAGE: `vr_left_controller_pad_down_tool_select`


## `vr_left_controller_pad_down_zoom`

Sets the left controller pad down mode to Zoom.

USAGE: `vr_left_controller_pad_down_zoom`


## `vr_left_controller_trigger_click_effect`

Emulates the trigger click effect for the left controller.

USAGE: `vr_left_controller_trigger_click_effect`


## `vr_left_controller_zoom_scale`

Controls the size of the zoomed object.

USAGE: `vr_left_controller_zoom_scale [value]`

Displays value of `vr_left_controller_zoom_scale`.  If value parameter provided then sets `vr_left_controller_zoom_scale` to value specified.




## `vr_mode_display_network_players`

Determines whether other VR players will be rendered (0 = None, 1 = Controllers, 2 = Head + Controllers).

USAGE: `vr_mode_display_network_players [value]`

Displays value of `vr_mode_display_network_players`.  If value parameter provided then sets `vr_mode_display_network_players` to value specified.




## `vr_mode_hand_view`

Controls whether the virtual hand view is disabled, or attached to the left or right controller.

USAGE: `vr_mode_hand_view <mode>`

<mode> may be one of:

 0 = Detached (turned off)

 1 = Attached to Left controller

 2 = Attached to Right controller


## `vr_mode_icon_colored`

If ON then the icon showing the current tool mode will be colored instead of black.

USAGE: `vr_mode_icon_colored [ON|OFF|TOGGLE]`

Displays value of `vr_mode_icon_colored`.  If value parameter provided then sets `vr_mode_icon_colored` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_mode_icon_colored` = '`vr_mode_icon_colored TOGGLE`'


## `vr_mode_selection_style`

Chooses how drag-selection works in VR: a box of fixed height, a box drawn by the player, or a box anchored to the table.

USAGE: `vr_mode_selection_style [value]`

Displays value of `vr_mode_selection_style`.  If value parameter provided then sets `vr_mode_selection_style` to value specified.




## `vr_mode_ui_attachment`

Controls whether the screen UI is detached, or attached to the left or right controller.

USAGE: `vr_mode_ui_attachment <mode>`

<mode> may be one of:

 0 = Detached

 1 = Attached to Left controller

 2 = Attached to Right controller


## `vr_move_friction`

Amount of friction applied to inertia when vr_move_with_inertia is ON.

USAGE: `vr_move_friction [value]`

Displays value of `vr_move_friction`.  If value parameter provided then sets `vr_move_friction` to value specified.




## `vr_move_with_inertia`

When ON you will be able to throw yourself around when moving.

USAGE: `vr_move_with_inertia [ON|OFF|TOGGLE]`

Displays value of `vr_move_with_inertia`.  If value parameter provided then sets `vr_move_with_inertia` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_move_with_inertia` = '`vr_move_with_inertia TOGGLE`'


## `vr_orient_object_delay`

Delay in seconds after pickup in which the click effect will not register.

USAGE: `vr_orient_object_delay [value]`

Displays value of `vr_orient_object_delay`.  If value parameter provided then sets `vr_orient_object_delay` to value specified.




## `vr_right_controller_attach_hand_view`

Attached the virtual hand view to the right controller.

USAGE: `vr_right_controller_attach_hand_view`


## `vr_right_controller_bind_tool_hotkeys`

When ON the right controller's default tool selection hotkeys will be bound to its pad.

USAGE: `vr_right_controller_bind_tool_hotkeys [ON|OFF|TOGGLE]`

Displays value of `vr_right_controller_bind_tool_hotkeys`.  If value parameter provided then sets `vr_right_controller_bind_tool_hotkeys` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_right_controller_bind_tool_hotkeys` = '`vr_right_controller_bind_tool_hotkeys TOGGLE`'


## `vr_right_controller_mode_pad_down`

Controls whether pad down on the right controller is bindable, displays the tool selecter, or zooms the active object.

USAGE: `vr_right_controller_mode_pad_down <mode>`

<mode> may be one of:

 0 = Bindable

 1 = Tool Select

 2 = Zoom


## `vr_right_controller_pad_down_bindable`

Sets the right controller pad down mode to Bindable.

USAGE: `vr_right_controller_pad_down_bindable`


## `vr_right_controller_pad_down_tool_select`

Sets the right controller pad down mode to Tool Select.

USAGE: `vr_right_controller_pad_down_tool_select`


## `vr_right_controller_pad_down_zoom`

Sets the right controller pad down mode to Zoom.

USAGE: `vr_right_controller_pad_down_zoom`


## `vr_right_controller_trigger_click_effect`

Emulates the trigger click effect for the right controller.

USAGE: `vr_right_controller_trigger_click_effect`


## `vr_right_controller_zoom_scale`

Controls the size of the zoomed object.

USAGE: `vr_right_controller_zoom_scale [value]`

Displays value of `vr_right_controller_zoom_scale`.  If value parameter provided then sets `vr_right_controller_zoom_scale` to value specified.




## `vr_scale_rotate_rate`

When you scale/rotate in VR your movement is smoothed.  This sets how fast you approach the desired position.
Three values: <scale> <rotation> <position>

USAGE: `vr_scale_rotate_rate [x y z]`

Displays value of `vr_scale_rotate_rate`.

If [x y z] parameters provided then sets `vr_scale_rotate_rate` to value specified.




## `vr_selection_height`

Sets height of VR selection box when not using exact selection.

USAGE: `vr_selection_height [value]`

Displays value of `vr_selection_height`.  If value parameter provided then sets `vr_selection_height` to value specified.




## `vr_selection_style_anchored`

Sets VR selection mode to a box which is anchored to the table.

USAGE: `vr_selection_style_anchored`


## `vr_selection_style_exact`

Sets VR selection mode to a box drawn by the player.

USAGE: `vr_selection_style_exact`


## `vr_selection_style_fixed`

Sets VR selection mode to a box of fixed height (which is set with vr_selection_height).

USAGE: `vr_selection_style_fixed`


## `vr_show_missing_binding_warning`

When ON, and when the GRAB and MAIN MENU actions are not bound, displays a warning advising how to set bindings.

USAGE: `vr_show_missing_binding_warning [ON|OFF|TOGGLE]`

Displays value of `vr_show_missing_binding_warning`.  If value parameter provided then sets `vr_show_missing_binding_warning` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_show_missing_binding_warning` = '`vr_show_missing_binding_warning TOGGLE`'


## `vr_spectator_replaces_main_window`

If ON then the spectator view will replace the normal display mirror.  If OFF then a second screen will open (requires second monitor).

USAGE: `vr_spectator_replaces_main_window [ON|OFF|TOGGLE]`

Displays value of `vr_spectator_replaces_main_window`.  If value parameter provided then sets `vr_spectator_replaces_main_window` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_spectator_replaces_main_window` = '`vr_spectator_replaces_main_window TOGGLE`'


## `vr_steamvr_bindings`

Lists all current SteamVR bindings.

USAGE: `vr_steamvr_bindings`


## `vr_sticky_grab`

If ON then grabbing control becomes sticky: press to grab and press again to release.

USAGE: `vr_sticky_grab [ON|OFF|TOGGLE]`

Displays value of `vr_sticky_grab`.  If value parameter provided then sets `vr_sticky_grab` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_sticky_grab` = '`vr_sticky_grab TOGGLE`'


## `vr_teleport_with_pad`

If ON then pushing up on the pad will let you teleport, if OFF you may 'bind' it.

USAGE: `vr_teleport_with_pad [ON|OFF|TOGGLE]`

Displays value of `vr_teleport_with_pad`.  If value parameter provided then sets `vr_teleport_with_pad` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_teleport_with_pad` = '`vr_teleport_with_pad TOGGLE`'


## `vr_thumbstick_icons_constant`

If ON then VR thumbstick icons are always displayed.

USAGE: `vr_thumbstick_icons_constant [ON|OFF|TOGGLE]`

Displays value of `vr_thumbstick_icons_constant`.  If value parameter provided then sets `vr_thumbstick_icons_constant` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_thumbstick_icons_constant` = '`vr_thumbstick_icons_constant TOGGLE`'


## `vr_tilt_angle`

Angle to use when tilting world.  It is advisable to turn tilt mode off while changing this setting!

USAGE: `vr_tilt_angle [value]`

Displays value of `vr_tilt_angle`.  If value parameter provided then sets `vr_tilt_angle` to value specified.




## `vr_tilt_mode`

Rotate the world around the Z axis.  Caution!

USAGE: `vr_tilt_mode [ON|OFF|TOGGLE]`

Displays value of `vr_tilt_mode`.  If value parameter provided then sets `vr_tilt_mode` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_tilt_mode` = '`vr_tilt_mode TOGGLE`'


## `vr_tooltips_action_enabled`

If ON then VR controller tooltips are displayed whenever the Display Tooltips action is activated.

USAGE: `vr_tooltips_action_enabled [ON|OFF|TOGGLE]`

Displays value of `vr_tooltips_action_enabled`.  If value parameter provided then sets `vr_tooltips_action_enabled` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_tooltips_action_enabled` = '`vr_tooltips_action_enabled TOGGLE`'


## `vr_tooltips_constant`

If ON then VR controller tooltips are always displayed.

USAGE: `vr_tooltips_constant [ON|OFF|TOGGLE]`

Displays value of `vr_tooltips_constant`.  If value parameter provided then sets `vr_tooltips_constant` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_tooltips_constant` = '`vr_tooltips_constant TOGGLE`'


## `vr_tooltips_for_click_when_on_menu`

If ON then VR controller tooltips are displayed for click action when on menu.

USAGE: `vr_tooltips_for_click_when_on_menu [ON|OFF|TOGGLE]`

Displays value of `vr_tooltips_for_click_when_on_menu`.  If value parameter provided then sets `vr_tooltips_for_click_when_on_menu` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_tooltips_for_click_when_on_menu` = '`vr_tooltips_for_click_when_on_menu TOGGLE`'


## `vr_tooltips_initial_duration`

Duration VR controller tooltip displays for at startup (when not set to be always-on).

USAGE: `vr_tooltips_initial_duration [value]`

Displays value of `vr_tooltips_initial_duration`.  If value parameter provided then sets `vr_tooltips_initial_duration` to value specified.




## `vr_ui_attach_left`

Attach VR screen UI to left controller.

USAGE: `vr_ui_attach_left`


## `vr_ui_attach_right`

Attach VR screen UI to right controller.

USAGE: `vr_ui_attach_right`


## `vr_ui_detached`

Detach VR screen UI.

USAGE: `vr_ui_detached`


## `vr_ui_floating`

When ON the VR UI screen will float in world space, or be attached to a controller (When OFF it will surround the room).

USAGE: `vr_ui_floating [ON|OFF|TOGGLE]`

Displays value of `vr_ui_floating`.  If value parameter provided then sets `vr_ui_floating` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_ui_floating` = '`vr_ui_floating TOGGLE`'


## `vr_ui_scale`

Sets size of VR UI screen when attached to controller.

USAGE: `vr_ui_scale [value]`

Displays value of `vr_ui_scale`.  If value parameter provided then sets `vr_ui_scale` to value specified.




## `vr_ui_suppressed`

When ON the VR UI screen will be hidden (but only if attached to a controller).

USAGE: `vr_ui_suppressed [ON|OFF|TOGGLE]`

Displays value of `vr_ui_suppressed`.  If value parameter provided then sets `vr_ui_suppressed` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_ui_suppressed` = '`vr_ui_suppressed TOGGLE`'


## `vr_unbind_all`

Removes all VR pad bindings.

Removes all commands bound to the VR controller pad.


## `vr_zoom_object_aligned`

If ON then when you active the object zoom on a controller, the magnified object will appear with the same orientation as the game object.

USAGE: `vr_zoom_object_aligned [ON|OFF|TOGGLE]`

Displays value of `vr_zoom_object_aligned`.  If value parameter provided then sets `vr_zoom_object_aligned` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!vr_zoom_object_aligned` = '`vr_zoom_object_aligned TOGGLE`'


## `wait`

Waits for the specified amount of time.  Useful in scripts.

USAGE: `wait <delay>`

Waits for <delay> seconds before executing the next command in a script.


## `zoom_always`

When ON (and when zoom_follows_pointer is OFF) the zoom display will always be displayed.

USAGE: `zoom_always [ON|OFF|TOGGLE]`

Displays value of `zoom_always`.  If value parameter provided then sets `zoom_always` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!zoom_always` = '`zoom_always TOGGLE`'


## `zoom_follow_pointer`

When ON the zoom display will appear at the pointer location. When OFF it will appear at zoom_position.

USAGE: `zoom_follow_pointer [ON|OFF|TOGGLE]`

Displays value of `zoom_follow_pointer`.  If value parameter provided then sets `zoom_follow_pointer` to value specified (if `TOGGLE` then its value is inverted).

Shortcut by prefixing with: `+ - !`

For example, `!zoom_follow_pointer` = '`zoom_follow_pointer TOGGLE`'


## `zoom_position`

The location the zoom display will appear when zoom_follows_pointer is off.  0,0 = bottom left, 1,1 = top right.

USAGE: `zoom_position [value]`

Display value of zoom_position.  If value parameter provided then sets zoom_position to value specified.
