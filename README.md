# Helmacs - Beginner-friendly Configurations for Helix and Emacs with a Common Base

Helmacs provides a unified, beginner-friendly configuration for both [Helix](https://helix-editor.com/) and [Emacs](https://www.gnu.org/software/emacs/), designed to make these powerful editors accessible to newcomers while maintaining their flexibility and power.

## Why Helmacs?

Helix and Emacs represent two ends of the editor spectrum: Helix offers a streamlined, out-of-the-box experience with minimal configuration, while Emacs is renowned for its deep customizability and extensibility. With Helmacs, you can use Helix for a fast, ready-to-use workflow, and seamlessly fall back to Emacs when you need advanced features or custom workflows that Helix may not (yet) provide. This approach gives you the best of both worlds—simplicity when you want it, and power when you need it.

### Flexibility
- **Input Methods**: Choose between keyboard-driven or mouse-based editing
- **Modal Editing**: Optional modal editing layer that can be enabled or disabled
- **Configuration**: Out-of-the-box and Customizabilty by the combination of Helix and Emacs

### Intuitive Design
- **Selection-First Approach**: Modal editing that starts with selection, making operations more predictable
- **Interactive Interfaces**: User-friendly menus and commands
- **Reduced Core Language**: Simplified set of keybindings that are easy to learn and remember

### Close to Defaults
- **Emacs**: Thin modal editing layer that preserves Emacs' native functionality
- **Helix**: Keybinding changes that maintain Helix's core design

## Core Features

### Unified Keybinding Language
Helmacs provides a consistent core set of keybindings across both editors, focusing on:

- **Modal Editing**: Intuitive text manipulation commands
- **Modifier Commands**: Familiar keyboard shortcuts for navigation and editing that always work
- **Space Menu**: Quick access to common operations

## Core Editing Language

Helmacs uses a reduced, intuitive, and consistent set of keybindings—the "core editing language"—shared between Helix and Emacs. This language is designed to be easy to learn, flexible, and powerful, supporting both modal and non-modal workflows. Note that this is an abstract specification: each editor may implement the exact behavior differently, especially in this early stage of the project. The goal is to provide a common mental model while allowing for editor-specific optimizations.

### General
| Key  | Action                 |
|------|------------------------|
| M-x  | Execute command        |
| C-g  | Cancel operation       |

### Prefix
| Key  | Action                      |
|------|-----------------------------|
| C-x  | General purpose prefix      |
| C-c  | Mode specific and user      |

### Modal
| Key  | Action                        |
|------|-------------------------------|
| esc  | Exit insert                   |
| i    | Insert                        |
| a    | Append                        |
| o    | Insert below                  |
| O    | Insert above                  |
| l    | Select line                   |
| e    | Expand selection              |
| E    | Shrink selection              |
| m    | Mark/match prefix             |
| k    | Cut (kill)                    |
| r    | Replace                       |
| w    | Copy                          |
| y    | Paste                         |
| .    | Contextual act                |
| u    | Undo                          |
| U    | Redo                          |
| j    | Jump                          |
| c    | Better access to C-c prefix   |
| x    | Better access to C-x prefix   |

### Modifier Command
| Key    | Action                    |
|--------|---------------------------|
| C-n    | Next line                 |
| C-p    | Previous line             |
| C-b    | Backward char             |
| C-f    | Forward char              |
| M-b    | Backward word             |
| M-f    | Forward word              |
| C-y    | Paste                     |
| M-w    | Copy                      |
| C-k    | Kill to line end          |
| C-d    | Delete char forward       |
| M-d    | Delete word forward       |
| M-DEL  | Delete word backward      |
| C-a    | Go line start             |
| C-e    | Go line end               |
| M-m    | Go first nonwhitespace    |
| M-<    | Go buffer beginning       |
| M->    | Go buffer end             |
| C-v    | Page down                 |
| M-v    | Page up                   |
| C-l    | Recenter                  |
| M-r    | Go window center          |
| C-s    | Search forward            |
| C-r    | Search backward           |
| M-.    | Goto definition           |
| M-,    | Jump backward             |

### Space Menu (Accessed via SPC)
| Key   | Action                 |
|-------|------------------------|
| e     | Execute command        |
| r     | Split window right     |
| o     | Goto other window      |
| 1     | Delete other windows   |
| b     | Buffer search          |
| a     | Last buffer            |
| f/F   | File search            |
| s     | Line search project    |
| d     | Directory editor       |
| x,c   | Prefix commands        |
| j     | Jump                   |

## Setup

### Helix
1. Clone this repository
2. Run Helix with the configuration:
   ```bash
   helix -c /path/to/helmacs/helix/config.toml
   ```

### Emacs

#### Test setup

1. Clone this repository
2. Run the following in a terminal
   ```bash
   emacs --init-directory=/path/to/cloned/helmacs/emacs/
   ```

#### Permanent setup

1. Clone this repository
2. Create or update your Emacs configuration directory:
   ```bash
   # Create the directory if it doesn't exist (backup if it does)
   mkdir -p ~/.emacs.d
   
   # Copy the configuration files
   cp /path/to/helmacs/emacs/init.el ~/.emacs.d/
   
   # Symlink myinit.org and documentation folder
   ln -s /path/to/helmacs/emacs/myinit.org ~/.emacs.d/
   ln -s /path/to/helmacs/documentation ~/.emacs.d/
   ```
3. Start Emacs
4. For detailed setup and usage instructions, see: Main -> Documentation -> Getting started

## License

This project is dual licensed under both the MIT License and the Unlicense. You may choose either license at your option. See the [LICENSE-MIT](LICENSE-MIT) and [UNLICENSE](UNLICENSE) files for the full text of each license. 