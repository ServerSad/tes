# Server-UI Documentation

Documentação oficial da biblioteca de interface "NongkhawKawaii-UI".

## Inicialização da Biblioteca
```lua
local Env = loadstring(game:HttpGet("https://raw.githubusercontent.com/ServerSad/tes/refs/heads/main/Utilities/Server-UI.luau", true))()
```

## Criando uma Janela
```lua
local Window = Env:Window({
    Title = "Nome do Projeto",
    Desc = "Descrição do projeto"
})
```
- Title (string): Nome da interface.
- Desc (string): Descrição da interface.

## Criando uma Aba (Tab)
```lua
local Tab = Window:Add({
    Title = "Título da Aba",
    Desc = "Descrição da Aba",
    Banner = 123456789012345
})
```
- Title (string): Nome da aba.
- Desc (string): Texto descritivo.
- Banner (number): ID da imagem banner.

## Criando uma Seção
```lua
local Section = Tab:Section({
    Title = "Nome da Seção",
    Side = "l" -- ou "r"
})
```
- Title (string): Nome da seção.
- Side (string): Lado onde a seção aparecerá ('l' ou 'r').

## Botão
```lua
Section:Button({
    Title = "Clique Aqui",
    Desc = "Descrição do botão", -- opcional
    Icon = 123456789012345, -- opcional
    Callback = function()
        print("Botão pressionado")
    end
})
```

## Toggle (Ativador)
```lua
Section:Toggle({
    Title = "Ativar Algo",
    Desc = "Descrição do toggle", -- opcional
    Icon = 123456789012345, -- opcional
    Value = false,
    Callback = function(state)
        print(state)
    end
})
```

## TextBox
```lua
Section:Textbox({
    Value = "Texto Padrão",
    PlaceHolder = "Digite aqui...",
    ClearOnFocus = false,
    Callback = function(text)
        print(text)
    end
})
```

## Slider
```lua
Section:Slider({
    Title = "Controle Deslizante",
    Min = 0,
    Max = 100,
    Value = 50,
    Rounding = 2,
    CallBack = function(value)
        print(value)
    end
})
```

## Dropdown
```lua
Section:Dropdown({
    Title = "Selecione",
    Multi = true, -- ou false
    List = {"Opção 1", "Opção 2"},
    Value = {"Opção 1"}, -- para Multi = true
    Callback = function(selected)
        print(selected)
    end
})
```

## Keybind (Tecla de atalho)
```lua
Section:Keybind({
    Title = "Atalho",
    Key = Enum.KeyCode.E,
    Value = false,
    Callback = function(key, state)
        print(key, state)
    end
})
```

## Linha separadora
```lua
Section:Line()
```

## Discord (Convite ou ID)
```lua
Section:Discord("SeuServidor")
```

## Imagem de Banner
```lua
Section:ThumnailsImage({
    Banner = 123456789012345
})
```

## Parágrafo (Texto longo)
```lua
Section:Paragarp({
    Title = "Parágrafo",
    Desc = "Texto longo aqui explicando algo ou informando atualizações..."
})
```
