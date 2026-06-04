---
layout: page
title: fireclickdetector
---

```luau
fireclickdetector(ClickDetector)
```

fires the [ClickDetector](https://create.roblox.com/docs/reference/engine/classes/ClickDetector) when in range of [MaxActivationDistance](https://create.roblox.com/docs/reference/engine/classes/ClickDetector#MaxActivationDistance).

if you want to fire every [ClickDetector](https://create.roblox.com/docs/reference/engine/classes/ClickDetector):

- without tp
  ```luau
  for i v in game:GetDescendants() do
    if v:IsA("ClickDetector") then
       fireclickdetector(v)
    end
  end
  ```
- with tp
  ```luau
  local hrp = game.Players.LocalPlayer.Character.HumanoidRootPart
  local hrppos = hrp.CFrame
  for i v in game:GetDescendants() do
    if v:IsA("ClickDetector") then
       fireclickdetector(v)
       hrp.CFrame = v.CFrame
    end
  end
  hrp.CFrame = hrppos
  ```
