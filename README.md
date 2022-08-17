# obs-midi-mg

Allows MIDI devices to interact with OBS Studio.

### This plugin will not work in OBS Studio versions below 28.0.0 due to its usage of Qt 6, meaning that any users using an OS below Windows 10 or MacOS 10.15 will not be able to use this plugin.
(This may be addressed at a later date.)

### As of version 1.1.1, this plugin will display properly on both *Dark* and *Yami* themes.

## Description

Connect MIDI devices and seamlessly integrate with OBS Studio! This plugin offers:
- Easy setup
- Easy navigation
- Many customization options
- Cross-platform

## Installing

Go to the [Releases page](https://github.com/nhielost/obs-midi-mg/releases) and download and install the latest release for the proper operating system. That's it!

## Usage

To set up bindings, open OBS Studio and open the setup window under *Tools > obs-midi-mg Setup*. The setup window should appear.

If any MIDI devices are connected, they should appear in the ***Devices*** display on the left.
To access the bindings display, select the device to use for interacting with OBS Studio, and click *View Bindings* in the bottom right.

### Bindings

To add a binding, click the *Add* button in the bottom left. A new binding will appear in the ***Bindings*** display for the selected device.

To rename the binding, double-click the binding and type to change the name. To remove the binding (if needed), select the binding and click *Remove* in the bottom left.

To use a binding, messages and actions must be added. To add messages and actions, click *View Messages* and *View Actions* respectively.

### Messages

To add a message, click the *Add* button in the bottom left. A new message will appear in the ***Messages*** display for the selected binding.

To rename the message, double-click the message and type to change the name. To remove the message (if needed), select the message and click *Remove* in the bottom left.

To edit the message, select the message in the ***Messages*** display, and the editor will appear on the right.

Adjust the values as necessary for the message. By default, the value/velocity option is OFF for the use of its value in executing actions. If you wish to make the value required for executing an action, click the OFF in the middle of the value field, and it will switch to a number. Clicking the number again will revert it to the OFF state.

*Note: You can use multiple messages in a binding by adding more messages. If this is desired, the behavior of the binding may not be appropriate. See [Binding Modes](#binding-modes) for more details*.

### Actions

To add an action, click the *Add* button in the bottom left. A new message will appear in the ***Actions*** display for the selected binding.

To rename the action, double-click the action and type to change the name. To remove the action (if needed), select the action and click *Remove* in the bottom left.

To edit the action, select the action in the ***Actions*** display, and the editor will appear on the right.

Adjust the values as necessary for the action(s) in this binding. Settings will appear as the form is filled out. To use a value from a message, either click the number (the same way as the value field for messages) for the number fields, or select *Use Message Value* in the selection fields.

*Note: You can use multiple actions in a binding by adding more actions. If this is desired, the behavior of the binding may not be appropriate. See [Binding Modes](#binding-modes) for more details*.

### Binding Modes

When selecting a binding, a selection field will appear displaying the Binding Mode. Each mode changes how actions are executed, and which messages will be sent as values to each action. In all modes, messages will be evaluated before actions, and all actions will execute after the final message is received.

- **Consecutive Mode**: In this mode, actions can only use the final message as a value. This is the default mode, and should be used in most cases.
- **Correspondence Mode**: In this mode, actions can use the corresponding message as their value.
- **Multiply Mode**: In this mode, actions receive all previous messages as values. Only use this mode for multiple messages and singular actions as this may take a long time.

### Returning to a Previous Menu

To return to the menu before the current menu, click the *Return* button in the bottom left. The *Messages* and *Actions* menus will return to the *Bindings* menu, and the *Bindings* menu will return to the *Devices* menu.

### Preferences

To adjust other settings or view this page, click the *Preferences* button in the bottom left. Bindings can be exported and imported here, and the whole plugin can be turned off here as well.

## Future Content

The coming updates will hopefully introduce these new features:

- A transfer bindings between devices feature (for when a device has disconnected or is unavailable)
- Using more elements of the message than just the value (planned for 1.2.0)
- More actions involving external features such as Scene Collections, Themes, and other settings
- MIDI Output device support - send a message when an event in OBS Studio occurs (well underway!)

## Feedback

I would love to hear honestly from you about this plugin. Feel free to share some ideas and don't be afraid to report an issue!

[Click here to go to the Issues Page](https://github.com/nhielost/obs-midi-mg/issues).
