# `gethui`

`#!luau gethui` returns a **hidden [`#!luau Instance`](https://create.roblox.com/docs/reference/engine/classes/Instance)** container used for safely storing UI elements. This container is mainly designed to **avoid detections**.

```luau
function gethui(): BasePlayerGui | Folder
```

## Parameters

| Parameter | Description                        |
| --------- | ---------------------------------- |
| *(none)*  | This function takes no parameters. |

---

## Example

```luau title="Creating undetectable UI in gethui" linenums="1"
local hui = gethui() :: (BasePlayerGui | Folder)

local gui = Instance.new("ScreenGui", hui)
gui.Name = "GUI"

local label = Instance.new("TextLabel", gui)
label.Size = UDim2.fromOffset(200, 50)
label.Text = "Hello from gethui!"

print(hui:FindFirstChild("GUI")) -- Output: GUI
```
