# Vex-V5-82777W-Code

Robot code for VEX V5 team 82777W. It's built with [PROS](https://pros.cs.purdue.edu/) (kernel 3.8.0) and [EZ-Template](https://ez-robotics.github.io/EZ-Template/) 2.2.0.

## 1. Clone the code

You need [Git](https://git-scm.com/downloads) installed. Open a terminal and run:

```
git clone https://github.com/vex-v5/Vex-V5-82777W-Code.git
cd Vex-V5-82777W-Code/EZ-Template-Example-Proj-2.2.0
```

To get your teammates' latest changes later, run `git pull`.

## 2. Install PROS

1. Install [Visual Studio Code](https://code.visualstudio.com/).
2. In VS Code, open the **Extensions** panel (`Ctrl+Shift+X`), search for **PROS**, and install the extension from **sigbots**.
3. Restart VS Code. The first time it starts, the extension downloads the PROS command-line tool and the compiler. Let it finish.
4. Check that it worked: open a terminal in VS Code (`` Ctrl+` ``) and run `pros --version`.

You don't need to install EZ-Template separately. It's already included in this project (`firmware/EZ-Template.a` and `include/EZ-Template/`). Keep it at version 2.2.0. The code is written for 2.2.0's functions, and newer versions won't compile it.

## 3. Compile and upload

In VS Code, use **File > Open Folder** to open the `EZ-Template-Example-Proj-2.2.0` folder. Then run these commands in the VS Code terminal:

| Command | What it does |
|---|---|
| `pros make` | Compile only. Use this to check for errors. |
| `pros upload` | Upload the last build to the robot. |
| `pros mu` | Compile **and** upload in one step. Shows upload progress. |

To upload:

1. Connect the V5 Brain or the controller to the computer with a USB cable. The controller works over its wireless link to the Brain.
2. Make sure the Brain is on, and close any program that's running on it.
3. Run `pros mu`.
4. Run the program from the Brain screen or the controller.

You can also use the buttons in the PROS sidebar in VS Code (Build, Upload, Build & Upload) instead of typing the commands.

## Tips

- If an upload fails, close the program running on the Brain or controller first, then try again.
- The joystick-axis drive code (`Controller1.Axis3` / `Axis4`) in `opcontrol()` is commented out and doesn't work yet. The robot currently drives with EZ-Template's `chassis.arcade_standard(ez::SINGLE)`.
