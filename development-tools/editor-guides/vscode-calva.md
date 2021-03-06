# VSCode and Calva user guide

Open the VSCode editor and start a REPL for your project.  Then add your Clojure project and connect to your REPL.

> ####HINT::MacOSX Keys - Option or Alt
> Depending on the version of Mac computer you use, your Alt key may be called Option
> So `Ctrl+Alt+cv e` would be `Ctrl+Option+v e`

## Open Project Folder in VSCode

`Ctrl+k Ctrl+o` to open the Folder that contains your project.  Or using the menu **File** > **Open Folder**

Select the top level of the folder, e.g. `playground` and click **OK**



Start a REPL project and connect: .
Answer the quick-pick prompts telling Calva about project types and what profiles to start.


## Start a REPL for the project using Leiningen.

`ctrl+alt+c ctrl+alt+j` to start a REPL.

Select or type `Leiningen` when prompted for the project type

![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-project-type.png)

Wait a few moments for the REPL to start.

A new CLJ REPL tab will open when the Clojure REPL is ready


![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-repl-tab.png)

### Troubleshooting

If the REPL did not start, the nREPL link in the bottom blue bar will show the word "Disconnected".

![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-nrepl-button.png)

Open the Output tab to see the progress of the REPL starting.  Ask your coach for help if you see output other than that below.

![VS Code - Calva - Start REPL - nREPL button](/images/vscode-calva-clojure-repl-connect-output.png)



## Developing your project ##

Once you have a running REPL, use these commands to help you develop your code.

> ####HINT::MacOSX Keys - Option or Alt
> Depending on the version of Mac computer you use, your Alt key may be called Option
> So `Ctrl+Alt+c e` would be `Ctrl+Option+c e`

| Evaluate code             | Keybinding         | Description                                                          |
|---------------------------|--------------------|----------------------------------------------------------------------|
| Namespace                 | `Ctrl+Alt+c n`     | [Broken] Evaluate the current namespace and change namespace in REPL |
| All code in Namespace     | `Ctrl+Alt+c alt+n` | Evaluate all the code in current namespace                           |
| Outer expression          | `Ctrl+Alt+c SPACE` | Show the result of the top level expression                          |
| Expression                | `Ctrl+Alt+c e`     | Show the result of the current expression                            |
| Expression (send to REPL) | `Ctrl+Alt+c alt+e` | Send expression to the REPL and evaluate                             |
| Pretty print              | `Ctrl+Alt+c p`     | Print expression so its easier to read                               |
| Replace expression        | `Ctrl+Alt+c r`     | Replace the expression with its result                               |
| In the REPL               | `Enter`      | Code in the REPL window is evaluated                                 |

You can run tests from Calva too...

| Tests to run            | Keybinding           | Description                             |
|-------------------------|----------------------|-----------------------------------------|
| All tests               | `Ctrl+Alt+c Shift+t` | Run all tests in the project            |
| Current Namespace tests | `Ctrl+Alt+c t`       | Run all tests for the current namespace |
| Re-run failing tests | `Ctrl+Alt+c Ctrl+t`  | Run all tests for the current namespace |

> ####HINT::REPL history
> The REPL maintains a history of the code typed in and can be navigated by using the up and down arrow keys.


## Commenting / uncommenting code

Type `;;` at the start of a line to comment out the whole line.

> ####TODO::Comment keybindings ?


## Increase / decrease font size

`Ctrl +` and `Ctrl -` will increase and decrease the size of the whole editor.


## Structured editing - Paredit

Once you get the basics of Clojure development, you can try structural editing which is a way to refactor you code without breaking the structure of Clojure.  Structural editing ensures you dont have uneven parentheses, `()`, `[]`, `{}`, etc.

Please look at the [documentation for Calva Paredit](https://github.com/BetterThanTomorrow/calva-paredit/blob/master/README.md) to make use of Structural editing.


---

## Starting a remote REPL (old approach)
**Ctrl+`** toggles open the [VSCode Integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal).  Or open your operating system terminal.

> ####INFO::Windows GitBash users
> [Configure the Atom internal terminal to use the GitBash shell](https://code.visualstudio.com/docs/editor/integrated-terminal#_configuration).

In the terminal, change to the folder than contains your project, e.g. `cd projects/clojure/playground`

Type the command `lein repl` in the terminal.

![Calva Atom Terminal - Clojure REPL running](/images/vscode-calva-terminal-repl-running.png)


### Connecting to a Remote REPL from Calva

`Ctrl+Alt+c c` will open a command pop-up asking you to enter **host** and **port**. These details were shown when the REPL was run in the terminal.

![Calva - connect to running REPL](/images/vscode-calva-connect-host-and-port.png)

In the bottom left of Atom, check the status of the **nrepl** connection.  If you are connected, then the *disconnected* status should disappear

![Calva - nrepl disconnected](/images/vscode-calva-nrepl-disconnected.png)
