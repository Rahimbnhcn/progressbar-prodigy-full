# Echo Prodigy 2.0 Inspired Progressbar {STANDALONE}

# Preview

https://media.discordapp.net/attachments/1212949487908159540/1294714057365917706/image.png?ex=670c03ed&is=670ab26d&hm=15a63aacb52b85fe64c411175ca5eac2957b2c48fc68f42c2f7bf3e8c124a12c&=&format=webp&quality=lossless&width=455&height=77


# Usage

## QB-Core Functions

### Client

- QBCore.Functions.Progressbar(**name**: string, **label**: string, **duration**: number, **useWhileDead**: boolean, **canCancel**: boolean, **disableControls**: table, **animation**: table, **prop**: table, **propTwo**: table, **onFinish**: function, **onCancel**: function)
  > Create a new progressbar from the built in qb-core functions.<br>
  > **Example:**
  > ```lua
  >QBCore.Functions.Progressbar("random_task", "Karma is the best..", 5000, false, true, {
  >    disableMovement = false,
  >    disableCarMovement = false,
  >    disableMouse = false,
  >    disableCombat = true,
  >}, {
  >    animDict = "mp_suicide",
  >    anim = "pill",
  >    flags = 49,
  >}, {}, {}, function()
  >    -- Done
  >end, function()
  >    -- Cancel
  >end)
  > ```

## Exports

### Client

- Progress(**data**: string, **handler**: function)
  > Creates a new progress bar directly from the export, always use the built in qb-core function if possible.<br>
  > **Example:**
  > ```lua
  >exports['progressbar']:Progress({
  >    name = "random_task",
  >    duration = 5000,
  >    label = "I love ANTUNES..",
  >    useWhileDead = false,
  >    canCancel = true,
  >    controlDisables = {
  >        disableMovement = false,
  >        disableCarMovement = false,
  >        disableMouse = false,
  >        disableCombat = true,
  >    },
  >    animation = {
  >        animDict = "mp_suicide",
  >        anim = "pill",
  >        flags = 49,
  >    },
  >    prop = {},
  >    propTwo = {}
  >}, function(cancelled)
  >    if not cancelled then
  >        -- finished
  >    else
  >        -- cancelled
  >    end
  >end)
  > ```
  > **Props Example:**
  > ```lua
  >exports['progressbar']:Progress({
  >    name = "random_task",
  >    duration = 5000,
  >    label = "Prodigy2.0 Progressbar..",
  >    useWhileDead = false,
  >    canCancel = true,
  >    controlDisables = {
  >        disableMovement = false,
  >        disableCarMovement = false,
  >        disableMouse = false,
  >        disableCombat = true,
  >    },
  >    animation = {
  >        animDict = "missheistdockssetup1clipboard@base",
  >        anim = "pill",
  >        flags = 49,
  >    },
  >    prop = {
  >      model = 'prop_notepad_01',
  >      bone = 18905,
  >      coords = vec3(0.1, 0.02, 0.05),
  >      rotation = vec3(10.0, 0.0, 0.0),
  >    },
  >    propTwo = {
  >      model = 'prop_pencil_01',
  >      bone = 58866,
  >      coords = vec3(0.11, -0.02, 0.001),
  >      rotation = vec3(-120.0, 0.0, 0.0),
  >    }
  >}, function(cancelled)
  >    if not cancelled then
  >        -- finished
  >    else
  >        -- cancelled
  >    end
  >end)
  > ```

 
