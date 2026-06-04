---
title: lerp
---

# [Lerp](https://create.roblox.com/docs/reference/engine/datatypes/CFrame#Lerp)

```luau
CF:Lerp(
    goal:CF, alpha:NUM
)
```

| params | returns |
|:-------|:--------|
| goal   | CF      |
| alpha  |         |

returns a CF interpolated between itself and goal by the fraction of alpha\
example:

```luau
local part = Workspace.Part

while task.wait() do
     if not part.CFrame == CFrame.new(0,5,0) then
        part.CFrame:Lerp(CFrame.new(0,5,0), 4)
     end
end
```
