--[[
    Custom UI Library V3 (Premium Clean)
    All features working + Icons for notifications
    
    REFACTORED: All variables/functions stored in _0xd5fe table
]]

---------------------------------------------------------------------
-- _0xd5fe TABLE SETUP (Central storage for all library state)
---------------------------------------------------------------------
local _0xd5fe = {}
setmetatable(_0xd5fe, {
    __index = function(t, k)
        local v = rawget(t, k)
        if v ~= nil then return v end
        return _G[k]
    end,
    __newindex = function(t, k, v)
        rawset(t, k, v)
    end
})

-- Services stored in _0xd5fe
_0xd5fe._0x8efd = game:GetService("UserInputService")
_0xd5fe._0xa4bd = game:GetService("TweenService")
_0xd5fe._0x7f0f = game:GetService("CoreGui")
_0xd5fe._0x785d = game:GetService("Players")
_0xd5fe._0x740e = game:GetService("HttpService")

_0xd5fe._0x0e5f = {
    Open = true,
    ToggleKey = Enum.KeyCode.RightControl,
    AccentColor = Color3.fromRGB(96, 76, 255),
    Font = Enum.Font.GothamMedium,
    FontBold = Enum.Font.GothamBold,
    Theme = {
        Background = Color3.fromRGB(18, 18, 22),
        Sidebar = Color3.fromRGB(22, 22, 28),
        Section = Color3.fromRGB(25, 25, 32),
        Element = Color3.fromRGB(32, 32, 42),
        Text = Color3.fromRGB(245, 245, 250),
        TextDim = Color3.fromRGB(130, 130, 145),
        Outline = Color3.fromRGB(45, 45, 58),
        Shadow = Color3.fromRGB(0, 0, 0),
        Accent = Color3.fromRGB(96, 76, 255),
        Success = Color3.fromRGB(76, 209, 139),
        Error = Color3.fromRGB(255, 85, 85),
        Warning = Color3.fromRGB(255, 193, 59),
    },
    Icons = {
        check = "rbxassetid://10709790644",
        error = "rbxassetid://10747384394",
        info = "rbxassetid://10723415903",
        warning = "rbxassetid://10709753149",
        shield = "rbxassetid://10734951847",
        eye = "rbxassetid://10723346959",
        settings = "rbxassetid://10734950309",
        search = "rbxassetid://10734943674",
        user = "rbxassetid://10747373176",
        heart = "rbxassetid://10723406885",
        star = "rbxassetid://10734966248",
        bell = "rbxassetid://10709775704",
        home = "rbxassetid://10723407389",
        folder = "rbxassetid://10723387563",
        file = "rbxassetid://10723374641",
        download = "rbxassetid://10723344270",
        upload = "rbxassetid://10747366434",
        trash = "rbxassetid://10747362393",
        edit = "rbxassetid://10734883598",
        copy = "rbxassetid://10709812159",
        save = "rbxassetid://10734941499",
        refresh = "rbxassetid://10734933222",
        play = "rbxassetid://10734923549",
        pause = "rbxassetid://10734919336",
        stop = "rbxassetid://10734972621",
        power = "rbxassetid://10734930466",
        lock = "rbxassetid://10723434711",
        unlock = "rbxassetid://10747366027",
        key = "rbxassetid://10723416652",
        target = "rbxassetid://10734977012",
        crosshair = "rbxassetid://10709818534",
        zap = "rbxassetid://10723345749",
        flame = "rbxassetid://10723376114",
        sword = "rbxassetid://10734975486",
        swords = "rbxassetid://10734975692",
        gamepad = "rbxassetid://10723395457",
        mouse = "rbxassetid://10734898592",
        keyboard = "rbxassetid://10723416765",
        monitor = "rbxassetid://10734896881",
        cpu = "rbxassetid://10709813383",
        database = "rbxassetid://10709818996",
        server = "rbxassetid://10734949856",
        wifi = "rbxassetid://10747382504",
        bluetooth = "rbxassetid://10709776655",
        globe = "rbxassetid://10723404337",
        map = "rbxassetid://10734886202",
        compass = "rbxassetid://10709811445",
        navigation = "rbxassetid://10734906744",
        rocket = "rbxassetid://10734934585",
        plane = "rbxassetid://10734922971",
        car = "rbxassetid://10709789810",
        truck = "rbxassetid://10747364031",
        bike = "rbxassetid://10709775894",
        train = "rbxassetid://10747362105",
        ship = "rbxassetid://10734941354",
        anchor = "rbxassetid://10709761530",
        crown = "rbxassetid://10709818626",
        trophy = "rbxassetid://10747363809",
        medal = "rbxassetid://10734887072",
        gem = "rbxassetid://10723396000",
        diamond = "rbxassetid://10709819149",
        coins = "rbxassetid://10709811110",
        wallet = "rbxassetid://10747376205",
        gift = "rbxassetid://10723396402",
        package = "rbxassetid://10734909540",
        box = "rbxassetid://10709782497",
        archive = "rbxassetid://10709762233",
        inbox = "rbxassetid://10723415335",
        mail = "rbxassetid://10734885430",
        message = "rbxassetid://10734888228",
        phone = "rbxassetid://10734921524",
        camera = "rbxassetid://10709789686",
        image = "rbxassetid://10723415040",
        video = "rbxassetid://10747374938",
        music = "rbxassetid://10734905958",
        headphones = "rbxassetid://10723406165",
        mic = "rbxassetid://10734888864",
        volume = "rbxassetid://10747376008",
        speaker = "rbxassetid://10734965419",
        sun = "rbxassetid://10734974297",
        moon = "rbxassetid://10734897102",
        cloud = "rbxassetid://10709806740",
        rain = "rbxassetid://10709806277",
        snow = "rbxassetid://10734964600",
        wind = "rbxassetid://10747382750",
        thermometer = "rbxassetid://10734983134",
        droplet = "rbxassetid://10723344432",
        leaf = "rbxassetid://10723425539",
        tree = "rbxassetid://10747362534",
        flower = "rbxassetid://10747830374",
        bug = "rbxassetid://10709782845",
        skull = "rbxassetid://10734962068",
        ghost = "rbxassetid://10723396107",
        bot = "rbxassetid://10709782230",
        smile = "rbxassetid://10734964441",
        frown = "rbxassetid://10723394681",
        meh = "rbxassetid://10734887603",
        laugh = "rbxassetid://10723424372",
        angry = "rbxassetid://10709761629",
        party = "rbxassetid://10734918735",
        cake = "rbxassetid://10709783217",
        pizza = "rbxassetid://10734922774",
        coffee = "rbxassetid://10709810814",
        beer = "rbxassetid://10709775167",
        apple = "rbxassetid://10709761889",
        cookie = "rbxassetid://10709812067",
        code = "rbxassetid://10709810463",
        terminal = "rbxassetid://10734982144",
        command = "rbxassetid://10709811365",
        hash = "rbxassetid://10723405975",
        at = "rbxassetid://10709769286",
        link = "rbxassetid://10723426722",
        paperclip = "rbxassetid://10734910927",
        scissors = "rbxassetid://10734942778",
        clipboard = "rbxassetid://10709799288",
        bookmark = "rbxassetid://10709782154",
        tag = "rbxassetid://10734976528",
        flag = "rbxassetid://10723375890",
        pin = "rbxassetid://10734922324",
        layers = "rbxassetid://10723424505",
        layout = "rbxassetid://10723425376",
        grid = "rbxassetid://10723404936",
        list = "rbxassetid://10723433811",
        menu = "rbxassetid://10734887784",
        filter = "rbxassetid://10723375128",
        sliders = "rbxassetid://10734963400",
        maximize = "rbxassetid://10734886735",
        minimize = "rbxassetid://10734895698",
        expand = "rbxassetid://10723346553",
        shrink = "rbxassetid://10734953073",
        move = "rbxassetid://10734900011",
        grab = "rbxassetid://10723404472",
        hand = "rbxassetid://10723405649",
        pointer = "rbxassetid://10734929723",
        cursor = "rbxassetid://10734898476",
        plus = "rbxassetid://10734924532",
        minus = "rbxassetid://10734896206",
        x = "rbxassetid://10747384394",
        divide = "rbxassetid://10723343805",
        equal = "rbxassetid://10723345990",
        percent = "rbxassetid://10734919919",
        hash2 = "rbxassetid://10723405975",
        infinity = "rbxassetid://10723415766",
        circle = "rbxassetid://10709798174",
        square = "rbxassetid://10734965702",
        triangle = "rbxassetid://10747363621",
        hexagon = "rbxassetid://10723407092",
        octagon = "rbxassetid://10734907361",
        arrow_up = "rbxassetid://10709768939",
        arrow_down = "rbxassetid://10709767827",
        arrow_left = "rbxassetid://10709768114",
        arrow_right = "rbxassetid://10709768347",
        chevron_up = "rbxassetid://10709791523",
        chevron_down = "rbxassetid://10709790948",
        chevron_left = "rbxassetid://10709791281",
        chevron_right = "rbxassetid://10709791437",
        rotate_cw = "rbxassetid://10734940654",
        rotate_ccw = "rbxassetid://10734940376",
        undo = "rbxassetid://10747365484",
        redo = "rbxassetid://10734932822",
        repeat1 = "rbxassetid://10734933966",
        shuffle = "rbxassetid://10734953451",
        skip_back = "rbxassetid://10734961526",
        skip_forward = "rbxassetid://10734961809",
        rewind = "rbxassetid://10734934347",
        fast_forward = "rbxassetid://10723354521",
        loader = "rbxassetid://10723434070",
        clock = "rbxassetid://10709805144",
        timer = "rbxassetid://10734984606",
        hourglass = "rbxassetid://10723407498",
        calendar = "rbxassetid://10709789505",
        alarm = "rbxassetid://10709752630",
        stopwatch = "rbxassetid://10734984606",
        history = "rbxassetid://10723407335",
        activity = "rbxassetid://10709752035",
        pulse = "rbxassetid://10723406795",
        chart = "rbxassetid://10709773755",
        trending_up = "rbxassetid://10747363465",
        trending_down = "rbxassetid://10747363205",
        gauge = "rbxassetid://10723395708",
        speedometer = "rbxassetid://10723395708",
        battery = "rbxassetid://10709774640",
        battery_low = "rbxassetid://10709774370",
        battery_charging = "rbxassetid://10709774068",
        plug = "rbxassetid://10709790202",
        lightbulb = "rbxassetid://10723425852",
        flashlight = "rbxassetid://10723376471",
        lamp = "rbxassetid://10723417513",
        torch = "rbxassetid://10723376114",
        magnet = "rbxassetid://10723435069",
        compass2 = "rbxassetid://10709811445",
        ruler = "rbxassetid://10734941018",
        scale = "rbxassetid://10734941912",
        wrench = "rbxassetid://10747383470",
        hammer = "rbxassetid://10723405360",
        screwdriver = "rbxassetid://10747383470",
        axe = "rbxassetid://10709769508",
        shovel = "rbxassetid://10734952773",
        pickaxe = "rbxassetid://10709769508",
        brush = "rbxassetid://10709782758",
        paintbrush = "rbxassetid://10734910187",
        palette = "rbxassetid://10734910430",
        pipette = "rbxassetid://10734922497",
        eraser = "rbxassetid://10723346158",
        pencil = "rbxassetid://10734919691",
        pen = "rbxassetid://10734919503",
        highlighter = "rbxassetid://10723407192",
        type = "rbxassetid://10747364761",
        bold = "rbxassetid://10747813908",
        italic = "rbxassetid://10723416195",
        underline = "rbxassetid://10747365191",
        strikethrough = "rbxassetid://10734973290",
        align_left = "rbxassetid://10709759764",
        align_center = "rbxassetid://10709753570",
        align_right = "rbxassetid://10709759895",
        align_justify = "rbxassetid://10709759610",
        indent = "rbxassetid://10723415494",
        outdent = "rbxassetid://10734907933",
        quote = "rbxassetid://10734931234",
        heading = "rbxassetid://10723405975",
        paragraph = "rbxassetid://10734929981",
        text = "rbxassetid://10747364761",
        font = "rbxassetid://10747364761",
        subscript = "rbxassetid://10734973457",
        superscript = "rbxassetid://10734974850",
        book = "rbxassetid://10709781824",
        library = "rbxassetid://10723425615",
        newspaper = "rbxassetid://10734907168",
        scroll = "rbxassetid://10734943448",
        graduation = "rbxassetid://10723404691",
        award = "rbxassetid://10709769406",
        certificate = "rbxassetid://10709769406",
        badge = "rbxassetid://10709769406",
        verified = "rbxassetid://10747374131",
        fingerprint = "rbxassetid://10723375250",
        scan = "rbxassetid://10734942565",
        qr = "rbxassetid://10747360675",
        barcode = "rbxassetid://10747360675"
    }
}

_0xd5fe._0xd4c2 = nil

_0xd5fe._0x38c6 = function(gui)
    local success = false
    
    -- Try gethui first (most hidden)
    pcall(function()
        if gethui then
            local _cloneref = cloneref or function(x) return x end
            gui.Parent = _cloneref(gethui())
            success = true
        end
    end)
    
    if success then return end
    
    -- Try syn.protect_gui
    pcall(function()
        if syn and syn.protect_gui then
            local _cloneref = cloneref or function(x) return x end
            syn.protect_gui(gui)
            gui.Parent = _cloneref(_0xd5fe._0x7f0f)
            success = true
        end
    end)
    
    if success then return end
    
    -- Fallback to CoreGui with cloneref
    pcall(function()
        local _cloneref = cloneref or function(x) return x end
        gui.Parent = _cloneref(_0xd5fe._0x7f0f)
        success = true
    end)
    
    if success then return end
    
    -- Last resort - direct CoreGui
    pcall(function()
        gui.Parent = _0xd5fe._0x7f0f
    end)
end

_0xd5fe._0x36b7 = function(class, properties)
    local instance = Instance.new(class)
    for k, v in pairs(properties) do instance[k] = v end
    return instance
end

_0xd5fe._0xfb1b = function(parent, transparency)
    local Shadow = _0xd5fe._0x36b7("ImageLabel", {
        Name = "Shadow",
        Parent = parent,
        BackgroundTransparency = 1,
        Position = UDim2.new(0, -15, 0, -15),
        Size = UDim2.new(1, 30, 1, 30),
        Image = "rbxassetid://6014261993",
        ImageColor3 = _0xd5fe._0x0e5f.Theme.Shadow,
        ImageTransparency = transparency or 0.5,
        SliceCenter = Rect.new(49, 49, 450, 450),
        ScaleType = Enum.ScaleType.Slice,
        ZIndex = parent.ZIndex - 1
    })
    return Shadow
end

_0xd5fe._0x02b5 = function(trigger, object)
    local dragging, dragInput, dragStart, startPos
    trigger.InputBegan:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 then
            dragging = true
            dragStart = input.Position
            startPos = object.Position
            input.Changed:Connect(function() if input.UserInputState == Enum.UserInputState.End then dragging = false end end)
        end
    end)
    trigger.InputChanged:Connect(function(input) 
        if input.UserInputType == Enum.UserInputType.MouseMovement then dragInput = input end 
    end)
    _0xd5fe._0x8efd.InputChanged:Connect(function(input) 
        if input == dragInput and dragging then
            local delta = input.Position - dragStart
            _0xd5fe._0xa4bd:Create(object, TweenInfo.new(0.05), {Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)}):Play()
        end 
    end)
end

-- Notification System with Icons
function _0xd5fe._0x0e5f:Notify(Title, Content, Duration, IconType)
    if not _0xd5fe._0xd4c2 then return end
    Duration = Duration or 3
    IconType = IconType or "info"
    
    local Notif = _0xd5fe._0x36b7("Frame", {
        Parent = _0xd5fe._0xd4c2,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section,
        Size = UDim2.new(1, -10, 0, 0),
        BorderSizePixel = 0,
        ClipsDescendants = true
    })
    _0xd5fe._0x36b7("UICorner", {Parent = Notif, CornerRadius = UDim.new(0, 6)})
    _0xd5fe._0x36b7("UIStroke", {Parent = Notif, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
    
    local Icon = _0xd5fe._0x36b7("ImageLabel", {
        Parent = Notif,
        BackgroundTransparency = 1,
        Position = UDim2.new(0, 10, 0, 10),
        Size = UDim2.new(0, 30, 0, 30),
        Image = _0xd5fe._0x0e5f.Icons[IconType] or _0xd5fe._0x0e5f.Icons.info,
        ImageColor3 = _0xd5fe._0x0e5f.AccentColor
    })
    
    local TitleLbl = _0xd5fe._0x36b7("TextLabel", {
        Parent = Notif, 
        Text = Title, 
        Position = UDim2.new(0, 48, 0, 8), 
        Size = UDim2.new(1, -56, 0, 16), 
        Font = _0xd5fe._0x0e5f.FontBold, 
        TextColor3 = _0xd5fe._0x0e5f.Theme.Text, 
        TextSize = 13, 
        TextXAlignment = Enum.TextXAlignment.Left, 
        BackgroundTransparency = 1
    })
    
    local ContentLbl = _0xd5fe._0x36b7("TextLabel", {
        Parent = Notif, 
        Text = Content, 
        Position = UDim2.new(0, 48, 0, 26), 
        Size = UDim2.new(1, -56, 0, 1000), 
        Font = _0xd5fe._0x0e5f.Font, 
        TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, 
        TextSize = 12, 
        TextXAlignment = Enum.TextXAlignment.Left, 
        TextYAlignment = Enum.TextYAlignment.Top,
        BackgroundTransparency = 1,
        TextWrapped = true
    })
    
    local Bar = _0xd5fe._0x36b7("Frame", {
        Parent = Notif, 
        BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor, 
        Position = UDim2.new(0, 0, 0, 0), 
        Size = UDim2.new(0, 3, 1, 0), 
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = Bar, CornerRadius = UDim.new(0, 6)})
    
    -- Calculate height based on content text
    local textBounds = game:GetService("TextService"):GetTextSize(
        Content, 
        12, 
        _0xd5fe._0x0e5f.Font, 
        Vector2.new(290 - 56, 1000)
    )
    local contentHeight = math.max(textBounds.Y, 14)
    local notifHeight = math.max(50, 26 + contentHeight + 10)
    
    ContentLbl.Size = UDim2.new(1, -56, 0, contentHeight)
    
    _0xd5fe._0xa4bd:Create(Notif, TweenInfo.new(0.3), {Size = UDim2.new(1, -10, 0, notifHeight)}):Play()
    task.delay(Duration, function()
        _0xd5fe._0xa4bd:Create(Notif, TweenInfo.new(0.3), {Size = UDim2.new(1, -10, 0, 0)}):Play()
        task.wait(0.3)
        Notif:Destroy()
    end)
end

function _0xd5fe._0x0e5f:CreateWindow(Settings)
    local Title = Settings.Title or "UI"
    local Logo = Settings.Logo
    local Acrylic = Settings.Acrylic or false
    local BrandingText = Settings.BrandingText
    local BrandingPosition = Settings.BrandingPosition or "bottom-left" -- "bottom-left", "top-left", "top-right"
    
    local ScreenGui = _0xd5fe._0x36b7("ScreenGui", { Name = _0xd5fe._0x740e:GenerateGUID(false), IgnoreGuiInset = true, ResetOnSpawn = false })
    _0xd5fe._0x38c6(ScreenGui)
    
    -- Branding watermark
    if BrandingText then
        local brandPos
        local brandAnchor = Vector2.new(0, 0)
        if BrandingPosition == "top-left" then
            brandPos = UDim2.new(0, 80, 0, 5) -- Right of chat icon
        elseif BrandingPosition == "top-right" then
            brandPos = UDim2.new(1, -10, 0, 5)
            brandAnchor = Vector2.new(1, 0) -- Anchor to right side
        else -- bottom-left default
            brandPos = UDim2.new(0, 10, 1, -30)
        end
        
        local BrandingLabel = _0xd5fe._0x36b7("TextLabel", {
            Parent = ScreenGui,
            Name = "Branding",
            BackgroundTransparency = 1,
            Position = brandPos,
            AnchorPoint = brandAnchor,
            Size = UDim2.new(0, 300, 0, 20),
            Text = BrandingText,
            Font = _0xd5fe._0x0e5f.FontBold,
            TextColor3 = _0xd5fe._0x0e5f.AccentColor,
            TextSize = 14,
            TextXAlignment = BrandingPosition == "top-right" and Enum.TextXAlignment.Right or Enum.TextXAlignment.Left,
            TextStrokeTransparency = 0.8,
            TextStrokeColor3 = Color3.new(0, 0, 0),
            ZIndex = 100
        })
        
        -- Store reference for potential updates
        _0xd5fe._0x0e5f.BrandingLabel = BrandingLabel
    end
    
    -- Loading Screen (same size as menu)
    local LoadingScreen = _0xd5fe._0x36b7("Frame", {
        Parent = ScreenGui,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Background,
        Position = UDim2.new(0.5, -375, 0.5, -275),
        Size = UDim2.new(0, 750, 0, 550),
        ZIndex = 1000,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = LoadingScreen, CornerRadius = UDim.new(0, 8)})
    _0xd5fe._0x36b7("UIStroke", {Parent = LoadingScreen, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
    _0xd5fe._0xfb1b(LoadingScreen, 0.2)
    
    local LoadingLogo = _0xd5fe._0x36b7("ImageLabel", {
        Parent = LoadingScreen,
        BackgroundTransparency = 1,
        Position = UDim2.new(0.5, 0, 0.4, 0),
        AnchorPoint = Vector2.new(0.5, 0.5),
        Size = UDim2.new(0, 350, 0, 350),
        Image = Logo or "rbxassetid://136163314754809",
        ZIndex = 1001,
        ScaleType = Enum.ScaleType.Fit
    })
    
    local LoadingBarOuter = _0xd5fe._0x36b7("Frame", {
        Parent = LoadingScreen,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element,
        Position = UDim2.new(0.5, 0, 0.7, 0),
        AnchorPoint = Vector2.new(0.5, 0.5),
        Size = UDim2.new(0, 300, 0, 24),
        ZIndex = 1001,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = LoadingBarOuter, CornerRadius = UDim.new(1, 0)})
    _0xd5fe._0x36b7("UIStroke", {Parent = LoadingBarOuter, Color = _0xd5fe._0x0e5f.AccentColor, Thickness = 2})
    
    local LoadingBarBg = _0xd5fe._0x36b7("Frame", {
        Parent = LoadingBarOuter,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section,
        Position = UDim2.new(0, 4, 0.5, 0),
        AnchorPoint = Vector2.new(0, 0.5),
        Size = UDim2.new(1, -8, 0, 14),
        ZIndex = 1002,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = LoadingBarBg, CornerRadius = UDim.new(1, 0)})
    
    local LoadingBar = _0xd5fe._0x36b7("Frame", {
        Parent = LoadingBarBg,
        BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor,
        Size = UDim2.new(0, 0, 1, 0),
        ZIndex = 1003,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = LoadingBar, CornerRadius = UDim.new(1, 0)})
    
    local LoadingText = _0xd5fe._0x36b7("TextLabel", {
        Parent = LoadingScreen,
        BackgroundTransparency = 1,
        Position = UDim2.new(0.5, 0, 0.78, 0),
        AnchorPoint = Vector2.new(0.5, 0),
        Size = UDim2.new(0, 300, 0, 20),
        Text = "Loading...",
        Font = _0xd5fe._0x0e5f.Font,
        TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
        TextSize = 14,
        ZIndex = 1001
    })
    
    -- Store reference to show main after loading
    local MainFrame = nil
    local function ShowMainAfterLoad()
        if MainFrame then
            MainFrame.Visible = true
        end
        _0xd5fe._0xa4bd:Create(LoadingScreen, TweenInfo.new(0.5), {BackgroundTransparency = 1}):Play()
        _0xd5fe._0xa4bd:Create(LoadingLogo, TweenInfo.new(0.5), {ImageTransparency = 1}):Play()
        _0xd5fe._0xa4bd:Create(LoadingBarOuter, TweenInfo.new(0.5), {BackgroundTransparency = 1}):Play()
        _0xd5fe._0xa4bd:Create(LoadingBarBg, TweenInfo.new(0.5), {BackgroundTransparency = 1}):Play()
        _0xd5fe._0xa4bd:Create(LoadingBar, TweenInfo.new(0.5), {BackgroundTransparency = 1}):Play()
        _0xd5fe._0xa4bd:Create(LoadingText, TweenInfo.new(0.5), {TextTransparency = 1}):Play()
        task.wait(0.5)
        LoadingScreen:Destroy()
    end
    
    -- Animate loading (5-8 seconds random)
    local loadDuration = math.random(50, 80) / 10
    _0xd5fe._0xa4bd:Create(LoadingBar, TweenInfo.new(loadDuration, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {Size = UDim2.new(1, 0, 1, 0)}):Play()
    task.delay(loadDuration, ShowMainAfterLoad)
    
    -- Notification Holder
    _0xd5fe._0xd4c2 = _0xd5fe._0x36b7("Frame", {
        Parent = ScreenGui,
        BackgroundTransparency = 1,
        Position = UDim2.new(1, -310, 1, -310),
        Size = UDim2.new(0, 300, 0, 300)
    })
    _0xd5fe._0x36b7("UIListLayout", {Parent = _0xd5fe._0xd4c2, Padding = UDim.new(0, 5), VerticalAlignment = Enum.VerticalAlignment.Bottom})

    -- Custom Cursor
    local CustomCursor = _0xd5fe._0x36b7("ImageLabel", {
        Parent = ScreenGui,
        Name = "CustomCursor",
        BackgroundTransparency = 1,
        Size = UDim2.new(0, 20, 0, 20),
        Image = "rbxassetid://102366537072878",
        ImageColor3 = _0xd5fe._0x0e5f.Theme.Text,
        ZIndex = 9999,
        Visible = true
    })
    
    local CursorShadow = _0xd5fe._0x36b7("ImageLabel", {
        Parent = CustomCursor,
        BackgroundTransparency = 1,
        Position = UDim2.new(0, 2, 0, 2),
        Size = UDim2.new(1, 0, 1, 0),
        Image = "rbxassetid://102366537072878",
        ImageColor3 = Color3.new(0, 0, 0),
        ImageTransparency = 0.7,
        ZIndex = 9998
    })
    
    local CursorDot = _0xd5fe._0x36b7("Frame", {
        Parent = ScreenGui,
        Name = "CursorDot",
        BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor,
        Size = UDim2.new(0, 6, 0, 6),
        ZIndex = 9999,
        Visible = true,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = CursorDot, CornerRadius = UDim.new(1, 0)})
    
    -- Tooltip Frame (follows mouse on hover)
    local Tooltip = _0xd5fe._0x36b7("Frame", {
        Parent = ScreenGui,
        Name = "Tooltip",
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Background,
        Size = UDim2.new(0, 0, 0, 32),
        AutomaticSize = Enum.AutomaticSize.XY,
        ZIndex = 10000,
        Visible = false,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = Tooltip, CornerRadius = UDim.new(0, 4)})
    _0xd5fe._0x36b7("UIPadding", {Parent = Tooltip, PaddingLeft = UDim.new(0, 8), PaddingRight = UDim.new(0, 8), PaddingTop = UDim.new(0, 6), PaddingBottom = UDim.new(0, 6)})
    
    local TooltipStroke = _0xd5fe._0x36b7("UIStroke", {Parent = Tooltip, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
    
    local TooltipLayout = _0xd5fe._0x36b7("UIListLayout", {
        Parent = Tooltip,
        FillDirection = Enum.FillDirection.Horizontal,
        VerticalAlignment = Enum.VerticalAlignment.Center,
        Padding = UDim.new(0, 6)
    })
    
    local TooltipIcon = _0xd5fe._0x36b7("ImageLabel", {
        Parent = Tooltip,
        Name = "Icon",
        BackgroundTransparency = 1,
        Size = UDim2.new(0, 14, 0, 14),
        LayoutOrder = 1,
        Image = _0xd5fe._0x0e5f.Icons.info,
        ImageColor3 = _0xd5fe._0x0e5f.Theme.Accent,
        ZIndex = 10001
    })
    
    local TooltipText = _0xd5fe._0x36b7("TextLabel", {
        Parent = Tooltip,
        Name = "Text",
        BackgroundTransparency = 1,
        Size = UDim2.new(0, 0, 0, 14),
        AutomaticSize = Enum.AutomaticSize.X,
        LayoutOrder = 2,
        Text = "",
        Font = _0xd5fe._0x0e5f.Font,
        TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
        TextSize = 12,
        TextXAlignment = Enum.TextXAlignment.Left,
        ZIndex = 10001
    })
    
    _0xd5fe._0x0e5f.Tooltip = Tooltip
    _0xd5fe._0x0e5f.TooltipIcon = TooltipIcon
    _0xd5fe._0x0e5f.TooltipText = TooltipText
    _0xd5fe._0x0e5f.TooltipStroke = TooltipStroke
    
    _0xd5fe._0x8efd.MouseIconEnabled = false
    
    local cursorConn = game:GetService("RunService").RenderStepped:Connect(function()
        -- Only update cursor when UI is visible to save FPS
        if not _0xd5fe._0x0e5f.Open then
            CustomCursor.Visible = false
            CursorDot.Visible = false
            return
        end
        
        CustomCursor.Visible = true
        CursorDot.Visible = true
        local mousePos = _0xd5fe._0x8efd:GetMouseLocation()
        CustomCursor.Position = UDim2.new(0, mousePos.X, 0, mousePos.Y)
        CursorDot.Position = UDim2.new(0, mousePos.X - 3, 0, mousePos.Y - 3)
        -- Update tooltip position to follow mouse
        if Tooltip.Visible then
            Tooltip.Position = UDim2.new(0, mousePos.X + 15, 0, mousePos.Y + 15)
        end
    end)
    
    -- Store cursor connection for cleanup
    _0xd5fe._0x0e5f.CursorConnection = cursorConn
    _0xd5fe._0x0e5f.CustomCursor = CustomCursor
    _0xd5fe._0x0e5f.CursorDot = CursorDot

    -- Main Window (hidden until loading completes)
    local Main = _0xd5fe._0x36b7("Frame", {
        Name = "Main",
        Parent = ScreenGui,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Background,
        BackgroundTransparency = Acrylic and 0.3 or 0,
        Position = UDim2.new(0.5, -375, 0.5, -275),
        Size = UDim2.new(0, 750, 0, 550),
        BorderSizePixel = 0,
        ClipsDescendants = false,
        Visible = false
    })
    MainFrame = Main
    _0xd5fe._0x36b7("UICorner", {Parent = Main, CornerRadius = UDim.new(0, 8)})
    _0xd5fe._0xfb1b(Main, 0.2)
    _0xd5fe._0x36b7("UIStroke", {Parent = Main, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})

    -- Store reference for acrylic toggle
    _0xd5fe._0x0e5f.MainFrame = Main
    _0xd5fe._0x0e5f.Acrylic = Acrylic
    
    function _0xd5fe._0x0e5f:SetAcrylic(enabled)
        _0xd5fe._0x0e5f.Acrylic = enabled
        local targetTransparency = enabled and 0.3 or 0
        _0xd5fe._0xa4bd:Create(_0xd5fe._0x0e5f.MainFrame, TweenInfo.new(0.3), {BackgroundTransparency = targetTransparency}):Play()
    end

    -- Resize handles
    local MIN_WIDTH = 600
    local MIN_HEIGHT = 400
    local HANDLE_SIZE = 8
    
    local function CreateResizeHandle(name, position, size, cursor)
        local handle = _0xd5fe._0x36b7("Frame", {
            Name = name,
            Parent = Main,
            BackgroundTransparency = 1,
            Position = position,
            Size = size,
            ZIndex = 10
        })
        return handle
    end
    
    -- Bottom-right corner (main resize handle)
    local ResizeBR = CreateResizeHandle("ResizeBR", 
        UDim2.new(1, -HANDLE_SIZE, 1, -HANDLE_SIZE), 
        UDim2.new(0, HANDLE_SIZE, 0, HANDLE_SIZE))
    
    -- Visual indicator for resize corner
    local ResizeIcon = _0xd5fe._0x36b7("Frame", {
        Parent = ResizeBR,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
        BackgroundTransparency = 0.5,
        Position = UDim2.new(0.5, -2, 0.5, -2),
        Size = UDim2.new(0, 4, 0, 4),
        ZIndex = 11
    })
    _0xd5fe._0x36b7("UICorner", {Parent = ResizeIcon, CornerRadius = UDim.new(1, 0)})
    
    -- Bottom edge
    local ResizeB = CreateResizeHandle("ResizeB",
        UDim2.new(0, HANDLE_SIZE, 1, -HANDLE_SIZE),
        UDim2.new(1, -HANDLE_SIZE * 2, 0, HANDLE_SIZE))
    
    -- Right edge
    local ResizeR = CreateResizeHandle("ResizeR",
        UDim2.new(1, -HANDLE_SIZE, 0, 45),
        UDim2.new(0, HANDLE_SIZE, 1, -45 - HANDLE_SIZE))
    
    -- Resize logic
    local resizing = false
    local resizeType = nil
    local resizeStart = nil
    local startSize = nil
    local startPos = nil
    
    local function StartResize(handle, rType)
        handle.InputBegan:Connect(function(input)
            if input.UserInputType == Enum.UserInputType.MouseButton1 and not Minimized then
                resizing = true
                resizeType = rType
                resizeStart = Vector2.new(input.Position.X, input.Position.Y)
                startSize = Main.AbsoluteSize
                startPos = Main.AbsolutePosition
            end
        end)
        
        handle.MouseEnter:Connect(function()
            _0xd5fe._0xa4bd:Create(ResizeIcon, TweenInfo.new(0.15), {BackgroundTransparency = 0, BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
        end)
        handle.MouseLeave:Connect(function()
            if not resizing then
                _0xd5fe._0xa4bd:Create(ResizeIcon, TweenInfo.new(0.15), {BackgroundTransparency = 0.5, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
            end
        end)
    end
    
    StartResize(ResizeBR, "BR")
    StartResize(ResizeB, "B")
    StartResize(ResizeR, "R")
    
    _0xd5fe._0x8efd.InputChanged:Connect(function(input)
        if resizing and input.UserInputType == Enum.UserInputType.MouseMovement then
            local delta = Vector2.new(input.Position.X, input.Position.Y) - resizeStart
            local newWidth = startSize.X
            local newHeight = startSize.Y
            
            if resizeType == "BR" or resizeType == "R" then
                newWidth = math.max(MIN_WIDTH, startSize.X + delta.X)
            end
            if resizeType == "BR" or resizeType == "B" then
                newHeight = math.max(MIN_HEIGHT, startSize.Y + delta.Y)
            end
            
            Main.Size = UDim2.new(0, newWidth, 0, newHeight)
        end
    end)
    
    _0xd5fe._0x8efd.InputEnded:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 and resizing then
            resizing = false
            resizeType = nil
            _0xd5fe._0xa4bd:Create(ResizeIcon, TweenInfo.new(0.15), {BackgroundTransparency = 0.5, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
        end
    end)

    -- Topbar
    local Topbar = _0xd5fe._0x36b7("Frame", {
        Name = "Topbar",
        Parent = Main,
        BackgroundTransparency = 1,
        Size = UDim2.new(1, 0, 0, 45)
    })
    _0xd5fe._0x02b5(Topbar, Main)
    
    local hasLogo = Logo and Logo ~= ""
    
    if hasLogo then
        local LogoImg = _0xd5fe._0x36b7("ImageLabel", {
            Parent = Topbar,
            BackgroundTransparency = 1,
            Position = UDim2.new(0, 15, 0.5, -15),
            Size = UDim2.new(0, 30, 0, 30),
            Image = Logo,
            ScaleType = Enum.ScaleType.Fit,
            ZIndex = 2
        })
    end

    local TopTitle = _0xd5fe._0x36b7("TextLabel", {
        Parent = Topbar,
        BackgroundTransparency = 1,
        Position = UDim2.new(0, hasLogo and 55 or 20, 0, 0),
        Size = UDim2.new(1, hasLogo and -100 or -65, 1, 0),
        Font = _0xd5fe._0x0e5f.FontBold,
        Text = Title,
        TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
        TextSize = 19,
        TextXAlignment = Enum.TextXAlignment.Left,
        ZIndex = 2
    })
    
    local MinBtn = _0xd5fe._0x36b7("TextButton", {
        Parent = Topbar,
        BackgroundTransparency = 1,
        Position = UDim2.new(1, -45, 0, 0),
        Size = UDim2.new(0, 45, 1, 0),
        Text = "−",
        Font = _0xd5fe._0x0e5f.FontBold,
        TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
        TextSize = 26,
        AutoButtonColor = false,
        ZIndex = 2
    })
    
    MinBtn.MouseEnter:Connect(function() _0xd5fe._0xa4bd:Create(MinBtn, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play() end)
    MinBtn.MouseLeave:Connect(function() _0xd5fe._0xa4bd:Create(MinBtn, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() end)
    
    local Minimized = false
    MinBtn.MouseButton1Click:Connect(function()
        Minimized = not Minimized
        Main.ClipsDescendants = true
        if Minimized then
            _0xd5fe._0xa4bd:Create(Main, TweenInfo.new(0.3, Enum.EasingStyle.Quart), {Size = UDim2.new(0, 750, 0, 45)}):Play()
            MinBtn.Text = "+"
        else
            _0xd5fe._0xa4bd:Create(Main, TweenInfo.new(0.3, Enum.EasingStyle.Quart), {Size = UDim2.new(0, 750, 0, 550)}):Play()
            MinBtn.Text = "−"
            task.wait(0.3)
            Main.ClipsDescendants = false
        end
    end)

    -- Sidebar
    local Sidebar = _0xd5fe._0x36b7("Frame", {
        Name = "Sidebar",
        Parent = Main,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Sidebar,
        BackgroundTransparency = Acrylic and 0.3 or 0,
        Position = UDim2.new(0, 0, 0, 45),
        Size = UDim2.new(0, 200, 1, -45),
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UICorner", {Parent = Sidebar, CornerRadius = UDim.new(0, 8)})
    _0xd5fe._0x36b7("Frame", {Parent = Sidebar, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Sidebar, BackgroundTransparency = Acrylic and 0.3 or 0, Size = UDim2.new(1,0,0,10), Position = UDim2.new(0,0,0,0), BorderSizePixel = 0})

    local TabContainer = _0xd5fe._0x36b7("ScrollingFrame", {
        Parent = Sidebar,
        BackgroundTransparency = 1,
        Position = UDim2.new(0, 10, 0, 10),
        Size = UDim2.new(1, -20, 1, -20),
        ScrollBarThickness = 0,
        BorderSizePixel = 0
    })
    _0xd5fe._0x36b7("UIListLayout", {Parent = TabContainer, Padding = UDim.new(0, 6)})

    local Content = _0xd5fe._0x36b7("Frame", {
        Name = "Content",
        Parent = Main,
        BackgroundTransparency = 1,
        Position = UDim2.new(0, 215, 0, 55),
        Size = UDim2.new(1, -225, 1, -65)
    })

    _0xd5fe._0x8efd.InputBegan:Connect(function(input)
        if input.KeyCode == _0xd5fe._0x0e5f.ToggleKey then 
            _0xd5fe._0x0e5f.Open = not _0xd5fe._0x0e5f.Open 
            Main.Visible = _0xd5fe._0x0e5f.Open 
            CustomCursor.Visible = _0xd5fe._0x0e5f.Open
            CursorDot.Visible = _0xd5fe._0x0e5f.Open
            _0xd5fe._0x8efd.MouseIconEnabled = not _0xd5fe._0x0e5f.Open
        end
    end)

    local WindowObj = {}
    
    function WindowObj:AddTab(Name, IconId)
        local TabBtn = _0xd5fe._0x36b7("TextButton", {
            Parent = TabContainer,
            BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Background,
            Size = UDim2.new(1, 0, 0, 36),
            AutoButtonColor = false,
            Text = "",
            BackgroundTransparency = 1
        })
        _0xd5fe._0x36b7("UICorner", {Parent = TabBtn, CornerRadius = UDim.new(0, 6)})
        
        -- Purple indicator bar on left
        local TabIndicator = _0xd5fe._0x36b7("Frame", {
            Parent = TabBtn,
            BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor,
            Size = UDim2.new(0, 3, 0, 18),
            Position = UDim2.new(0, 0, 0.5, -9),
            BackgroundTransparency = 1,
            BorderSizePixel = 0
        })
        _0xd5fe._0x36b7("UICorner", {Parent = TabIndicator, CornerRadius = UDim.new(0, 2)})
        
        -- Tab Icon
        local TabIcon = nil
        if IconId then
            TabIcon = _0xd5fe._0x36b7("ImageLabel", {
                Parent = TabBtn,
                BackgroundTransparency = 1,
                Position = UDim2.new(0, 12, 0.5, -9),
                Size = UDim2.new(0, 18, 0, 18),
                Image = IconId,
                ImageColor3 = _0xd5fe._0x0e5f.Theme.TextDim
            })
        end
        
        local TitleLbl = _0xd5fe._0x36b7("TextLabel", {
            Parent = TabBtn,
            BackgroundTransparency = 1,
            Position = UDim2.new(0, IconId and 38 or 14, 0, 0),
            Size = UDim2.new(1, IconId and -38 or -14, 1, 0),
            Text = Name,
            Font = _0xd5fe._0x0e5f.Font,
            TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
            TextSize = 14,
            TextXAlignment = Enum.TextXAlignment.Left
        })
        
        local TabPage = _0xd5fe._0x36b7("Frame", {
            Parent = Content,
            BackgroundTransparency = 1,
            Size = UDim2.new(1, 0, 1, 0),
            Visible = false
        })
        
        local SubTopBar = _0xd5fe._0x36b7("Frame", {
            Parent = TabPage,
            BackgroundTransparency = 1,
            Size = UDim2.new(1, 0, 0, 35),
            Visible = false
        })
        _0xd5fe._0x36b7("UIListLayout", {
            Parent = SubTopBar, 
            FillDirection = Enum.FillDirection.Horizontal, 
            Padding = UDim.new(0, 20),
            HorizontalAlignment = Enum.HorizontalAlignment.Left
        })
        
        local DefaultContainer = _0xd5fe._0x36b7("ScrollingFrame", {
            Parent = TabPage,
            BackgroundTransparency = 1,
            Size = UDim2.new(1,0,1,0),
            ScrollBarThickness = 3,
            ScrollBarImageColor3 = _0xd5fe._0x0e5f.Theme.Outline,
            CanvasSize = UDim2.new(0,0,0,0),
            BorderSizePixel = 0
        })
        local Left = _0xd5fe._0x36b7("Frame", {Parent = DefaultContainer, BackgroundTransparency = 1, Size = UDim2.new(0.5, -8, 1, 0)})
        local Right = _0xd5fe._0x36b7("Frame", {Parent = DefaultContainer, BackgroundTransparency = 1, Size = UDim2.new(0.5, -8, 1, 0), Position = UDim2.new(0.5, 8, 0, 0)})
        _0xd5fe._0x36b7("UIListLayout", {Parent = Left, Padding = UDim.new(0, 12), SortOrder = Enum.SortOrder.LayoutOrder})
        _0xd5fe._0x36b7("UIListLayout", {Parent = Right, Padding = UDim.new(0, 12), SortOrder = Enum.SortOrder.LayoutOrder})
        
        local function Activate()
            for _, v in pairs(TabContainer:GetChildren()) do
                if v:IsA("TextButton") then 
                     _0xd5fe._0xa4bd:Create(v, TweenInfo.new(0.2), {BackgroundTransparency = 1}):Play()
                     local titleLabel = v:FindFirstChild("TextLabel")
                     if titleLabel then 
                         _0xd5fe._0xa4bd:Create(titleLabel, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 14}):Play()
                     end
                     local indicator = v:FindFirstChild("Frame")
                     if indicator then _0xd5fe._0xa4bd:Create(indicator, TweenInfo.new(0.2), {BackgroundTransparency = 1}):Play() end
                     local icon = v:FindFirstChild("ImageLabel")
                     if icon then _0xd5fe._0xa4bd:Create(icon, TweenInfo.new(0.2), {ImageColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() end
                end
            end
            _0xd5fe._0xa4bd:Create(TabBtn, TweenInfo.new(0.2), {BackgroundTransparency = 0.95}):Play()
            _0xd5fe._0xa4bd:Create(TitleLbl, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 15}):Play()
            _0xd5fe._0xa4bd:Create(TabIndicator, TweenInfo.new(0.2), {BackgroundTransparency = 0}):Play()
            if TabIcon then _0xd5fe._0xa4bd:Create(TabIcon, TweenInfo.new(0.2), {ImageColor3 = _0xd5fe._0x0e5f.AccentColor}):Play() end
            
            for _, v in pairs(Content:GetChildren()) do v.Visible = false end
            TabPage.Visible = true
        end
        TabBtn.MouseButton1Click:Connect(Activate)
        
        if #TabContainer:GetChildren() == 2 then Activate() end

        local Tab = { HasSubTabs = false }
        
        function Tab:AddSubTab(SubName)
            if not Tab.HasSubTabs then
                Tab.HasSubTabs = true
                SubTopBar.Visible = true
                DefaultContainer.Visible = false
            end
            
            local SubBtn = _0xd5fe._0x36b7("TextButton", {
                Parent = SubTopBar,
                BackgroundTransparency = 1,
                Text = SubName,
                Font = _0xd5fe._0x0e5f.FontBold,
                TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
                TextSize = 15,
                AutomaticSize = Enum.AutomaticSize.X,
                Size = UDim2.new(0,0,1,0),
                AutoButtonColor = false
            })
            
            local Indicator = _0xd5fe._0x36b7("Frame", {
                Parent = SubBtn,
                BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor,
                Position = UDim2.new(0,0,1,-3),
                Size = UDim2.new(1,0,0,3),
                BackgroundTransparency = 1,
                BorderSizePixel = 0
            })
            _0xd5fe._0x36b7("UICorner", {Parent = Indicator, CornerRadius = UDim.new(1,0)})
            
            local SubContent = _0xd5fe._0x36b7("ScrollingFrame", {
                Parent = TabPage,
                BackgroundTransparency = 1,
                Position = UDim2.new(0, 0, 0, 40),
                Size = UDim2.new(1, 0, 1, -40),
                ScrollBarThickness = 3,
                ScrollBarImageColor3 = _0xd5fe._0x0e5f.Theme.Outline,
                Visible = false,
                BorderSizePixel = 0
            })
            local SLeft = _0xd5fe._0x36b7("Frame", {Parent = SubContent, BackgroundTransparency = 1, Size = UDim2.new(0.5, -8, 1, 0)})
            local SRight = _0xd5fe._0x36b7("Frame", {Parent = SubContent, BackgroundTransparency = 1, Size = UDim2.new(0.5, -8, 1, 0), Position = UDim2.new(0.5, 8, 0, 0)})
            _0xd5fe._0x36b7("UIListLayout", {Parent = SLeft, Padding = UDim.new(0, 12), SortOrder = Enum.SortOrder.LayoutOrder})
            _0xd5fe._0x36b7("UIListLayout", {Parent = SRight, Padding = UDim.new(0, 12), SortOrder = Enum.SortOrder.LayoutOrder})
            
            SubBtn.MouseEnter:Connect(function() if Indicator.BackgroundTransparency == 1 then _0xd5fe._0xa4bd:Create(SubBtn, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play() end end)
            SubBtn.MouseLeave:Connect(function() if Indicator.BackgroundTransparency == 1 then _0xd5fe._0xa4bd:Create(SubBtn, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() end end)
            
            SubBtn.MouseButton1Click:Connect(function()
                for _,v in pairs(SubTopBar:GetChildren()) do 
                     if v:IsA("TextButton") then
                        _0xd5fe._0xa4bd:Create(v, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                        _0xd5fe._0xa4bd:Create(v.Frame, TweenInfo.new(0.2), {BackgroundTransparency = 1}):Play()
                     end
                end
                _0xd5fe._0xa4bd:Create(SubBtn, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                _0xd5fe._0xa4bd:Create(Indicator, TweenInfo.new(0.2), {BackgroundTransparency = 0}):Play()
                
                for _,v in pairs(TabPage:GetChildren()) do if v:IsA("ScrollingFrame") then v.Visible = false end end
                SubContent.Visible = true
            end)
            
            local subcount = 0 
            for _,v in pairs(SubTopBar:GetChildren()) do if v:IsA("GuiObject") then subcount = subcount + 1 end end
            if subcount == 2 then
                 _0xd5fe._0xa4bd:Create(SubBtn, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                 _0xd5fe._0xa4bd:Create(Indicator, TweenInfo.new(0.2), {BackgroundTransparency = 0}):Play()
                 SubContent.Visible = true
            end

            return {
                AddLeftGroupbox = function(self, Name) return self:CreateGroupbox(SLeft, Name) end,
                AddRightGroupbox = function(self, Name) return self:CreateGroupbox(SRight, Name) end,
                CreateGroupbox = Tab.CreateGroupbox
            }
        end
        
        function Tab:CreateGroupbox(Parent, Name)
            local Box = _0xd5fe._0x36b7("Frame", {
                Parent = Parent,
                BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section,
                Size = UDim2.new(1, 0, 0, 50),
                AutomaticSize = Enum.AutomaticSize.Y,
                BorderSizePixel = 0
            })
            _0xd5fe._0x36b7("UICorner", {Parent = Box, CornerRadius = UDim.new(0, 8)})
            
            local Header = _0xd5fe._0x36b7("TextLabel", {
                Parent = Box,
                BackgroundTransparency = 1,
                Position = UDim2.new(0, 12, 0, 0),
                Size = UDim2.new(1, -24, 0, 32),
                Text = Name,
                Font = _0xd5fe._0x0e5f.FontBold,
                TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
                TextSize = 14,
                TextXAlignment = Enum.TextXAlignment.Left
            })
            _0xd5fe._0x36b7("Frame", {Parent = Box, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Outline, Size = UDim2.new(1, 0, 0, 1), Position = UDim2.new(0,0,0,32), BorderSizePixel = 0})

            local Container = _0xd5fe._0x36b7("Frame", {
                Parent = Box,
                BackgroundTransparency = 1,
                Position = UDim2.new(0, 12, 0, 40),
                Size = UDim2.new(1, -24, 0, 0),
                AutomaticSize = Enum.AutomaticSize.Y
            })
            _0xd5fe._0x36b7("UIListLayout", {Parent = Container, SortOrder = Enum.SortOrder.LayoutOrder, Padding = UDim.new(0, 8)})
            _0xd5fe._0x36b7("UIPadding", {Parent = Box, PaddingBottom = UDim.new(0, 12)})

            local Group = {}
            Group._container = Container
            
            function Group:AddToggle(Text, Default, Callback, TooltipOptions)
                local Frame = _0xd5fe._0x36b7("TextButton", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,22), Text = "", AutoButtonColor = false})
                local Label = _0xd5fe._0x36b7("TextLabel", {Parent = Frame, BackgroundTransparency = 1, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 13, TextXAlignment=Enum.TextXAlignment.Left, Size = UDim2.new(1,-45,1,0)})
                
                -- Toggle switch (pill shape)
                local ToggleTrack = _0xd5fe._0x36b7("Frame", {Parent = Frame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Size = UDim2.new(0,36,0,18), Position = UDim2.new(1,-36,0,2), BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = ToggleTrack, CornerRadius = UDim.new(1, 0)})
                local TrackStroke = _0xd5fe._0x36b7("UIStroke", {Parent = ToggleTrack, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                -- Toggle knob (circle)
                local ToggleKnob = _0xd5fe._0x36b7("Frame", {Parent = ToggleTrack, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Text, Size = UDim2.new(0,14,0,14), Position = UDim2.new(0,2,0,2), BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = ToggleKnob, CornerRadius = UDim.new(1, 0)})
                
                Frame.MouseEnter:Connect(function() 
                    _0xd5fe._0xa4bd:Create(TrackStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play()
                    -- Show tooltip if options provided
                    if TooltipOptions and TooltipOptions.Text then
                        local tooltipType = TooltipOptions.Type or "info"
                        local tooltipColor = tooltipType == "warning" and _0xd5fe._0x0e5f.Theme.Warning or _0xd5fe._0x0e5f.Theme.Accent
                        local tooltipIcon = tooltipType == "warning" and _0xd5fe._0x0e5f.Icons.warning or _0xd5fe._0x0e5f.Icons.info
                        
                        _0xd5fe._0x0e5f.TooltipIcon.Image = tooltipIcon
                        _0xd5fe._0x0e5f.TooltipIcon.ImageColor3 = tooltipColor
                        _0xd5fe._0x0e5f.TooltipText.Text = TooltipOptions.Text
                        _0xd5fe._0x0e5f.TooltipStroke.Color = tooltipColor
                        _0xd5fe._0x0e5f.Tooltip.Visible = true
                    end
                end)
                Frame.MouseLeave:Connect(function() 
                    _0xd5fe._0xa4bd:Create(TrackStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play()
                    -- Hide tooltip
                    if TooltipOptions and TooltipOptions.Text then
                        _0xd5fe._0x0e5f.Tooltip.Visible = false
                    end
                end)
                
                local State = Default or false
                local ToggleObj = {
                    Type = "Toggle",
                    Value = State
                }
                
                local function Update(instant)
                    ToggleObj.Value = State
                    if instant then
                        if State then
                            ToggleTrack.BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor
                            ToggleKnob.Position = UDim2.new(1, -16, 0, 2)
                            Label.TextColor3 = _0xd5fe._0x0e5f.Theme.Text
                        else
                            ToggleTrack.BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element
                            ToggleKnob.Position = UDim2.new(0, 2, 0, 2)
                            Label.TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim
                        end
                    else
                        if State then 
                            _0xd5fe._0xa4bd:Create(ToggleTrack, TweenInfo.new(0.2), {BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play() 
                            _0xd5fe._0xa4bd:Create(ToggleKnob, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Position = UDim2.new(1, -16, 0, 2)}):Play()
                            _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                        else 
                            _0xd5fe._0xa4bd:Create(ToggleTrack, TweenInfo.new(0.2), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element}):Play()
                            _0xd5fe._0xa4bd:Create(ToggleKnob, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Position = UDim2.new(0, 2, 0, 2)}):Play()
                            _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.2), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                        end
                    end
                    pcall(Callback, State)
                end
                
                ToggleObj.Set = function(self, v) State = v self.Value = v Update(true) end
                
                Frame.MouseButton1Click:Connect(function() State = not State Update() end)
                Update()
                
                _0xd5fe._0x0e5f.Options[Text] = ToggleObj
                return ToggleObj
            end
            
            function Group:AddSlider(Text, Min, Max, Default, Callback)
                 local Frame = _0xd5fe._0x36b7("Frame", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,42)})
                 local Label = _0xd5fe._0x36b7("TextLabel", {Parent = Frame, BackgroundTransparency = 1, Text = Text, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Font = _0xd5fe._0x0e5f.Font, TextSize=13, Size = UDim2.new(1,0,0,16), TextXAlignment=Enum.TextXAlignment.Left})
                 
                 local Bg = _0xd5fe._0x36b7("Frame", {Parent = Frame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Size = UDim2.new(1,0,0,7), Position = UDim2.new(0,0,0,24), BorderSizePixel = 0})
                 _0xd5fe._0x36b7("UICorner", {Parent = Bg, CornerRadius = UDim.new(1,0)})
                 local BgStroke = _0xd5fe._0x36b7("UIStroke", {Parent = Bg, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                 
                 local Fill = _0xd5fe._0x36b7("Frame", {Parent = Bg, BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor, Size = UDim2.new(0,0,1,0), BorderSizePixel = 0})
                 _0xd5fe._0x36b7("UICorner", {Parent = Fill, CornerRadius = UDim.new(1,0)})
                 
                local Value = _0xd5fe._0x36b7("TextLabel", {Parent = Frame, BackgroundTransparency = 1, Text = tostring(Default), TextColor3 = _0xd5fe._0x0e5f.Theme.Text, Font=_0xd5fe._0x0e5f.Font, TextSize=13, Size = UDim2.new(1,0,0,16), TextXAlignment=Enum.TextXAlignment.Right})
                 
                 Bg.MouseEnter:Connect(function() _0xd5fe._0xa4bd:Create(BgStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play() _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play() end)
                 Bg.MouseLeave:Connect(function() _0xd5fe._0xa4bd:Create(BgStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() end)
                 
                 local CurrentValue = Default or Min
                 local SliderObj = {
                     Type = "Slider",
                     Value = CurrentValue
                 }
                 
                 local function Set(v, instant)
                     v = math.clamp(v, Min, Max)
                     CurrentValue = v
                     SliderObj.Value = v
                     if instant then
                         Fill.Size = UDim2.new((v-Min)/(Max-Min), 0, 1, 0)
                     else
                         _0xd5fe._0xa4bd:Create(Fill, TweenInfo.new(0.1), {Size = UDim2.new((v-Min)/(Max-Min), 0, 1, 0)}):Play()
                     end
                     Value.Text = math.floor(v*100)/100
                     pcall(Callback, v)
                 end
                 
                 SliderObj.Set = function(self, v) Set(v, true) end
                 
                 local Dragging = false
                 Bg.InputBegan:Connect(function(i) if i.UserInputType == Enum.UserInputType.MouseButton1 then Dragging = true Set(Min + ((Max-Min) * math.clamp((i.Position.X - Bg.AbsolutePosition.X)/Bg.AbsoluteSize.X, 0, 1))) end end)
                 _0xd5fe._0x8efd.InputEnded:Connect(function(i) if i.UserInputType == Enum.UserInputType.MouseButton1 then Dragging = false end end)
                 _0xd5fe._0x8efd.InputChanged:Connect(function(i) if Dragging and i.UserInputType == Enum.UserInputType.MouseMovement then Set(Min + ((Max-Min) * math.clamp((i.Position.X - Bg.AbsolutePosition.X)/Bg.AbsoluteSize.X, 0, 1))) end end)
                 Set(Default or Min)
                 
                 _0xd5fe._0x0e5f.Options[Text] = SliderObj
                 return SliderObj
            end
            
            function Group:AddDropdown(Text, Options, Default, Callback)
                local DropFrame = _0xd5fe._0x36b7("Frame", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,50), ClipsDescendants = false})
                local Label = _0xd5fe._0x36b7("TextLabel", {Parent = DropFrame, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(1,0,0,18), BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, TextSize = 13})
                
                local Btn = _0xd5fe._0x36b7("TextButton", {Parent = DropFrame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Size = UDim2.new(1,0,0,28), Position = UDim2.new(0,0,0,20), Text = "", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, AutoButtonColor = false, BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = Btn, CornerRadius = UDim.new(0,6)})
                local DropStroke = _0xd5fe._0x36b7("UIStroke", {Parent = Btn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                local BtnText = _0xd5fe._0x36b7("TextLabel", {Parent = Btn, Text = tostring(Default or "Select..."), BackgroundTransparency = 1, Position = UDim2.new(0,10,0,0), Size = UDim2.new(1,-40,1,0), Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, TextXAlignment = Enum.TextXAlignment.Left})
                
                local Arrow = _0xd5fe._0x36b7("ImageLabel", {Parent = Btn, Image = "rbxassetid://7072706796", ImageColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(0,16,0,16), Position = UDim2.new(1,-26,0.5,-8), BackgroundTransparency = 1, ScaleType = Enum.ScaleType.Fit})
                
                local ListFrame = _0xd5fe._0x36b7("Frame", {Parent = DropFrame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section, Position = UDim2.new(0,0,0,50), Size = UDim2.new(1,0,0,0), BorderSizePixel = 0, ZIndex = 50, ClipsDescendants = true})
                _0xd5fe._0x36b7("UICorner", {Parent = ListFrame, CornerRadius = UDim.new(0,6)})
                _0xd5fe._0x36b7("UIStroke", {Parent = ListFrame, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                local List = _0xd5fe._0x36b7("ScrollingFrame", {Parent = ListFrame, BackgroundTransparency = 1, Size = UDim2.new(1,0,1,0), Position = UDim2.new(0,0,0,0), BorderSizePixel = 0, ScrollBarThickness = 0, ScrollBarImageColor3 = _0xd5fe._0x0e5f.AccentColor, ZIndex = 51, CanvasSize = UDim2.new(0,0,0,0), AutomaticCanvasSize = Enum.AutomaticSize.Y})
                _0xd5fe._0x36b7("UIListLayout", {Parent = List, SortOrder = Enum.SortOrder.LayoutOrder, Padding = UDim.new(0,0)})
                
                local Open = false
                
                local DropdownObj = {
                    Type = "Dropdown",
                    Value = Default
                }
                
                local function CreateOption(opt)
                    local OptBtn = _0xd5fe._0x36b7("TextButton", {Parent = List, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,28), Text = "", AutoButtonColor = false, BorderSizePixel = 0, ZIndex = 52})
                    local OptText = _0xd5fe._0x36b7("TextLabel", {Parent = OptBtn, Text = opt, BackgroundTransparency = 1, Position = UDim2.new(0,10,0,0), Size = UDim2.new(1,-20,1,0), Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 13, TextXAlignment = Enum.TextXAlignment.Left, ZIndex = 53})
                    
                    OptBtn.MouseEnter:Connect(function() 
                        _0xd5fe._0xa4bd:Create(OptBtn, TweenInfo.new(0.1), {BackgroundTransparency = 0, BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play() 
                        _0xd5fe._0xa4bd:Create(OptText, TweenInfo.new(0.1), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                    end)
                    OptBtn.MouseLeave:Connect(function() 
                        _0xd5fe._0xa4bd:Create(OptBtn, TweenInfo.new(0.1), {BackgroundTransparency = 1}):Play() 
                        _0xd5fe._0xa4bd:Create(OptText, TweenInfo.new(0.1), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                    end)
                    OptBtn.MouseButton1Click:Connect(function()
                        BtnText.Text = opt
                        DropdownObj.Value = opt
                        Open = false
                        _0xd5fe._0xa4bd:Create(ListFrame, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Size = UDim2.new(1,0,0,0)}):Play()
                        _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.2), {Rotation = 0}):Play()
                        pcall(Callback, opt)
                    end)
                end
                
                DropdownObj.Set = function(self, v)
                    BtnText.Text = tostring(v)
                    self.Value = v
                    pcall(Callback, v)
                end
                
                DropdownObj.Refresh = function(self, newOptions)
                    for _, child in pairs(List:GetChildren()) do
                        if child:IsA("TextButton") then child:Destroy() end
                    end
                    Options = newOptions
                    for _, opt in pairs(Options) do
                        CreateOption(opt)
                    end
                end
                
                Btn.MouseEnter:Connect(function() 
                    _0xd5fe._0xa4bd:Create(DropStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play() 
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play() 
                    _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.15), {ImageColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
                end)
                Btn.MouseLeave:Connect(function() 
                    _0xd5fe._0xa4bd:Create(DropStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() 
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() 
                    _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.15), {ImageColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                end)
                
                Btn.MouseButton1Click:Connect(function()
                    Open = not Open
                    if Open then
                        local height = math.min(#Options * 28 + 6, 150)
                        _0xd5fe._0xa4bd:Create(ListFrame, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Size = UDim2.new(1,0,0,height)}):Play()
                        _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.2), {Rotation = 180}):Play()
                    else
                        _0xd5fe._0xa4bd:Create(ListFrame, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Size = UDim2.new(1,0,0,0)}):Play()
                        _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.2), {Rotation = 0}):Play()
                    end
                end)
                
                for _, opt in pairs(Options) do
                    CreateOption(opt)
                end
                
                _0xd5fe._0x0e5f.Options[Text] = DropdownObj
                return DropdownObj
            end
            
            function Group:AddMultiDropdown(Text, Options, Defaults, Callback)
                Defaults = Defaults or {}
                local DropFrame = _0xd5fe._0x36b7("Frame", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,50), ClipsDescendants = false})
                local Label = _0xd5fe._0x36b7("TextLabel", {Parent = DropFrame, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(1,0,0,18), BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, TextSize = 13})
                
                local Btn = _0xd5fe._0x36b7("TextButton", {Parent = DropFrame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Size = UDim2.new(1,0,0,28), Position = UDim2.new(0,0,0,20), Text = "", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, AutoButtonColor = false, BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = Btn, CornerRadius = UDim.new(0,6)})
                local DropStroke = _0xd5fe._0x36b7("UIStroke", {Parent = Btn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                local BtnText = _0xd5fe._0x36b7("TextLabel", {Parent = Btn, Text = "None selected", BackgroundTransparency = 1, Position = UDim2.new(0,10,0,0), Size = UDim2.new(1,-40,1,0), Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, TextXAlignment = Enum.TextXAlignment.Left, TextTruncate = Enum.TextTruncate.AtEnd})
                
                local Arrow = _0xd5fe._0x36b7("ImageLabel", {Parent = Btn, Image = "rbxassetid://7072706796", ImageColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(0,16,0,16), Position = UDim2.new(1,-26,0.5,-8), BackgroundTransparency = 1, ScaleType = Enum.ScaleType.Fit})
                
                local ListFrame = _0xd5fe._0x36b7("Frame", {Parent = DropFrame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section, Position = UDim2.new(0,0,0,50), Size = UDim2.new(1,0,0,0), BorderSizePixel = 0, ZIndex = 50, ClipsDescendants = true})
                _0xd5fe._0x36b7("UICorner", {Parent = ListFrame, CornerRadius = UDim.new(0,6)})
                _0xd5fe._0x36b7("UIStroke", {Parent = ListFrame, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                local List = _0xd5fe._0x36b7("ScrollingFrame", {Parent = ListFrame, BackgroundTransparency = 1, Size = UDim2.new(1,0,1,0), Position = UDim2.new(0,0,0,0), BorderSizePixel = 0, ScrollBarThickness = 0, ScrollBarImageColor3 = _0xd5fe._0x0e5f.AccentColor, ZIndex = 51, CanvasSize = UDim2.new(0,0,0,0), AutomaticCanvasSize = Enum.AutomaticSize.Y})
                _0xd5fe._0x36b7("UIListLayout", {Parent = List, SortOrder = Enum.SortOrder.LayoutOrder, Padding = UDim.new(0,0)})
                
                local Open = false
                local Selected = {}
                
                -- Initialize with defaults
                for _, v in pairs(Defaults) do
                    Selected[v] = true
                end
                
                local MultiDropdownObj = {
                    Type = "MultiDropdown",
                    Value = Selected
                }
                
                local function UpdateText()
                    local selectedList = {}
                    for opt, isSelected in pairs(Selected) do
                        if isSelected then
                            table.insert(selectedList, opt)
                        end
                    end
                    if #selectedList == 0 then
                        BtnText.Text = "None selected"
                    elseif #selectedList <= 3 then
                        BtnText.Text = table.concat(selectedList, ", ")
                    else
                        BtnText.Text = #selectedList .. " selected"
                    end
                end
                
                local function GetSelectedArray()
                    local arr = {}
                    for opt, isSelected in pairs(Selected) do
                        if isSelected then
                            table.insert(arr, opt)
                        end
                    end
                    return arr
                end
                
                local OptionButtons = {}
                
                local function CreateOption(opt)
                    local OptBtn = _0xd5fe._0x36b7("TextButton", {Parent = List, BackgroundTransparency = Selected[opt] and 0 or 1, BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor, Size = UDim2.new(1,0,0,28), Text = "", AutoButtonColor = false, BorderSizePixel = 0, ZIndex = 52})
                    local OptText = _0xd5fe._0x36b7("TextLabel", {Parent = OptBtn, Text = opt, BackgroundTransparency = 1, Position = UDim2.new(0,10,0,0), Size = UDim2.new(1,-20,1,0), Font = _0xd5fe._0x0e5f.Font, TextColor3 = Selected[opt] and _0xd5fe._0x0e5f.Theme.Text or _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 13, TextXAlignment = Enum.TextXAlignment.Left, ZIndex = 53})
                    
                    OptionButtons[opt] = {Btn = OptBtn, Text = OptText}
                    
                    local function UpdateOption()
                        if Selected[opt] then
                            _0xd5fe._0xa4bd:Create(OptBtn, TweenInfo.new(0.1), {BackgroundTransparency = 0, BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
                            _0xd5fe._0xa4bd:Create(OptText, TweenInfo.new(0.1), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                        else
                            _0xd5fe._0xa4bd:Create(OptBtn, TweenInfo.new(0.1), {BackgroundTransparency = 1}):Play()
                            _0xd5fe._0xa4bd:Create(OptText, TweenInfo.new(0.1), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                        end
                    end
                    
                    OptBtn.MouseEnter:Connect(function() 
                        if not Selected[opt] then
                            _0xd5fe._0xa4bd:Create(OptBtn, TweenInfo.new(0.1), {BackgroundTransparency = 0, BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
                        end
                        _0xd5fe._0xa4bd:Create(OptText, TweenInfo.new(0.1), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                    end)
                    OptBtn.MouseLeave:Connect(function() 
                        if not Selected[opt] then
                            _0xd5fe._0xa4bd:Create(OptBtn, TweenInfo.new(0.1), {BackgroundTransparency = 1}):Play()
                            _0xd5fe._0xa4bd:Create(OptText, TweenInfo.new(0.1), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                        end
                    end)
                    OptBtn.MouseButton1Click:Connect(function()
                        Selected[opt] = not Selected[opt]
                        UpdateOption()
                        UpdateText()
                        MultiDropdownObj.Value = Selected
                        pcall(Callback, GetSelectedArray())
                    end)
                end
                
                MultiDropdownObj.Set = function(self, selectedArray)
                    Selected = {}
                    for _, v in pairs(selectedArray) do
                        Selected[v] = true
                    end
                    self.Value = Selected
                    UpdateText()
                    -- Update visual state of all options
                    for opt, elements in pairs(OptionButtons) do
                        if Selected[opt] then
                            elements.Btn.BackgroundTransparency = 0
                            elements.Btn.BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor
                            elements.Text.TextColor3 = _0xd5fe._0x0e5f.Theme.Text
                        else
                            elements.Btn.BackgroundTransparency = 1
                            elements.Text.TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim
                        end
                    end
                    pcall(Callback, GetSelectedArray())
                end
                
                MultiDropdownObj.Refresh = function(self, newOptions)
                    for _, child in pairs(List:GetChildren()) do
                        if child:IsA("TextButton") then child:Destroy() end
                    end
                    OptionButtons = {}
                    Options = newOptions
                    for _, opt in pairs(Options) do
                        CreateOption(opt)
                    end
                    UpdateText()
                end
                
                Btn.MouseEnter:Connect(function() 
                    _0xd5fe._0xa4bd:Create(DropStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play() 
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play() 
                    _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.15), {ImageColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
                end)
                Btn.MouseLeave:Connect(function() 
                    _0xd5fe._0xa4bd:Create(DropStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() 
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() 
                    _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.15), {ImageColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                end)
                
                Btn.MouseButton1Click:Connect(function()
                    Open = not Open
                    if Open then
                        local height = math.min(#Options * 28 + 6, 180)
                        _0xd5fe._0xa4bd:Create(ListFrame, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Size = UDim2.new(1,0,0,height)}):Play()
                        _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.2), {Rotation = 180}):Play()
                    else
                        _0xd5fe._0xa4bd:Create(ListFrame, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {Size = UDim2.new(1,0,0,0)}):Play()
                        _0xd5fe._0xa4bd:Create(Arrow, TweenInfo.new(0.2), {Rotation = 0}):Play()
                    end
                end)
                
                for _, opt in pairs(Options) do
                    CreateOption(opt)
                end
                
                UpdateText()
                
                _0xd5fe._0x0e5f.Options[Text] = MultiDropdownObj
                return MultiDropdownObj
            end
            
            function Group:AddDivider()
                _0xd5fe._0x36b7("Frame", {
                    Parent = Container,
                    BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Outline,
                    Size = UDim2.new(1, 0, 0, 1),
                    BorderSizePixel = 0
                })
            end
            
            function Group:AddColorPicker(Text, Default, Callback)
                local Frame = _0xd5fe._0x36b7("Frame", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,26)})
                local Label = _0xd5fe._0x36b7("TextLabel", {Parent = Frame, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(1,-75,1,0), BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, TextSize = 13})
                
                local ColorBtn = _0xd5fe._0x36b7("TextButton", {Parent = Frame, BackgroundColor3 = Default or Color3.new(1,1,1), Size = UDim2.new(0,70,0,22), Position = UDim2.new(1,-70,0,2), Text = "", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 11, AutoButtonColor = false, BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = ColorBtn, CornerRadius = UDim.new(0,5)})
                local ColorStroke = _0xd5fe._0x36b7("UIStroke", {Parent = ColorBtn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                ColorBtn.MouseEnter:Connect(function() 
                    _0xd5fe._0xa4bd:Create(ColorStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play()
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                end)
                ColorBtn.MouseLeave:Connect(function() 
                    _0xd5fe._0xa4bd:Create(ColorStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play()
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                end)
                
                local function RGBToHSV(color)
                    local r, g, b = color.R, color.G, color.B
                    local max, min = math.max(r, g, b), math.min(r, g, b)
                    local h, s, v = 0, 0, max
                    local d = max - min
                    s = max == 0 and 0 or d / max
                    if max ~= min then
                        if max == r then h = (g - b) / d + (g < b and 6 or 0)
                        elseif max == g then h = (b - r) / d + 2
                        elseif max == b then h = (r - g) / d + 4
                        end
                        h = h / 6
                    end
                    return h, s, v
                end
                
                local initH, initS, initV = RGBToHSV(Default or Color3.new(1,1,1))
                local CurrentColor = {H = initH, S = initS, V = initV}
                local ActivePicker = nil
                
                ColorBtn.MouseButton1Click:Connect(function()
                    if ActivePicker and ActivePicker.Parent then
                        ActivePicker:Destroy()
                        ActivePicker = nil
                        return
                    end
                    
                    local mainPos = Main.AbsolutePosition
                    local pickerX = mainPos.X + Main.AbsoluteSize.X + 10
                    local pickerY = mainPos.Y + 50
                    local screenSize = workspace.CurrentCamera.ViewportSize
                    if pickerX + 280 > screenSize.X then pickerX = mainPos.X - 290 end
                    if pickerY + 320 > screenSize.Y then pickerY = screenSize.Y - 330 end
                    
                    local Picker = _0xd5fe._0x36b7("Frame", {Parent = ScreenGui, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section, Position = UDim2.new(0, pickerX, 0, pickerY), Size = UDim2.new(0, 280, 0, 310), BorderSizePixel = 0, ZIndex = 100})
                    ActivePicker = Picker
                    _0xd5fe._0x36b7("UICorner", {Parent = Picker, CornerRadius = UDim.new(0,8)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = Picker, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    _0xd5fe._0xfb1b(Picker, 0.3)
                    
                    local PickerTopbar = _0xd5fe._0x36b7("Frame", {Parent = Picker, BackgroundTransparency = 1, Size = UDim2.new(1, 0, 0, 32)})
                    _0xd5fe._0x02b5(PickerTopbar, Picker)
                    
                    _0xd5fe._0x36b7("TextLabel", {Parent = Picker, Text = "Color Picker", Position = UDim2.new(0,12,0,8), Size = UDim2.new(1,-50,0,20), Font = _0xd5fe._0x0e5f.FontBold, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 14, TextXAlignment = Enum.TextXAlignment.Left, BackgroundTransparency = 1, ZIndex = 101})
                    
                    local CloseX = _0xd5fe._0x36b7("TextButton", {Parent = Picker, Text = "×", Position = UDim2.new(1,-28,0,4), Size = UDim2.new(0,24,0,24), BackgroundTransparency = 1, Font = _0xd5fe._0x0e5f.FontBold, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 20, AutoButtonColor = false, ZIndex = 101})
                    CloseX.MouseEnter:Connect(function() _0xd5fe._0xa4bd:Create(CloseX, TweenInfo.new(0.15), {TextColor3 = Color3.fromRGB(255,100,100)}):Play() end)
                    CloseX.MouseLeave:Connect(function() _0xd5fe._0xa4bd:Create(CloseX, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play() end)
                    CloseX.MouseButton1Click:Connect(function() Picker:Destroy() ActivePicker = nil end)
                    
                    local SVPicker = _0xd5fe._0x36b7("ImageButton", {Parent = Picker, BackgroundColor3 = Color3.fromHSV(CurrentColor.H, 1, 1), Position = UDim2.new(0,12,0,38), Size = UDim2.new(1,-24,0,140), Image = "rbxassetid://4155801252", BorderSizePixel = 0, AutoButtonColor = false, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = SVPicker, CornerRadius = UDim.new(0,6)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = SVPicker, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    
                    local SVCursor = _0xd5fe._0x36b7("Frame", {Parent = SVPicker, BackgroundColor3 = Color3.new(1,1,1), Size = UDim2.new(0,12,0,12), AnchorPoint = Vector2.new(0.5,0.5), Position = UDim2.new(CurrentColor.S, 0, 1 - CurrentColor.V, 0), BorderSizePixel = 0, ZIndex = 102})
                    _0xd5fe._0x36b7("UICorner", {Parent = SVCursor, CornerRadius = UDim.new(1,0)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = SVCursor, Color = Color3.new(0,0,0), Thickness = 2})
                    
                    local HuePicker = _0xd5fe._0x36b7("ImageButton", {Parent = Picker, BackgroundColor3 = Color3.new(1,1,1), Position = UDim2.new(0,12,0,186), Size = UDim2.new(1,-24,0,16), Image = "rbxassetid://3641079629", ScaleType = Enum.ScaleType.Crop, BorderSizePixel = 0, AutoButtonColor = false, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = HuePicker, CornerRadius = UDim.new(0,4)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = HuePicker, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    
                    local HueCursor = _0xd5fe._0x36b7("Frame", {Parent = HuePicker, BackgroundColor3 = Color3.new(1,1,1), Size = UDim2.new(0,6,1,4), AnchorPoint = Vector2.new(0.5,0.5), Position = UDim2.new(CurrentColor.H, 0, 0.5, 0), BorderSizePixel = 0, ZIndex = 102})
                    _0xd5fe._0x36b7("UICorner", {Parent = HueCursor, CornerRadius = UDim.new(0,2)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = HueCursor, Color = Color3.new(0,0,0), Thickness = 1})
                    
                    _0xd5fe._0x36b7("TextLabel", {Parent = Picker, Text = "Preview", Position = UDim2.new(0,12,0,210), Size = UDim2.new(0,50,0,14), Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 11, BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, ZIndex = 101})
                    local Preview = _0xd5fe._0x36b7("Frame", {Parent = Picker, BackgroundColor3 = Color3.fromHSV(CurrentColor.H, CurrentColor.S, CurrentColor.V), Position = UDim2.new(0,12,0,226), Size = UDim2.new(0,50,0,30), BorderSizePixel = 0, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = Preview, CornerRadius = UDim.new(0,6)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = Preview, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    
                    _0xd5fe._0x36b7("TextLabel", {Parent = Picker, Text = "Hex", Position = UDim2.new(0,72,0,210), Size = UDim2.new(0,80,0,14), Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 11, BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, ZIndex = 101})
                    local HexBox = _0xd5fe._0x36b7("TextBox", {Parent = Picker, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Position = UDim2.new(0,72,0,226), Size = UDim2.new(0,90,0,30), Text = "", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, BorderSizePixel = 0, ClearTextOnFocus = false, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = HexBox, CornerRadius = UDim.new(0,6)})
                    local HexStroke = _0xd5fe._0x36b7("UIStroke", {Parent = HexBox, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    _0xd5fe._0x36b7("UIPadding", {Parent = HexBox, PaddingLeft = UDim.new(0,8)})
                    HexBox.Focused:Connect(function() _0xd5fe._0xa4bd:Create(HexStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play() end)
                    HexBox.FocusLost:Connect(function() _0xd5fe._0xa4bd:Create(HexStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() end)
                    
                    _0xd5fe._0x36b7("TextLabel", {Parent = Picker, Text = "RGB", Position = UDim2.new(0,172,0,210), Size = UDim2.new(0,96,0,14), Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, TextSize = 11, BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, ZIndex = 101})
                    local RBox = _0xd5fe._0x36b7("TextBox", {Parent = Picker, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Position = UDim2.new(0,172,0,226), Size = UDim2.new(0,30,0,30), Text = "255", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 12, BorderSizePixel = 0, TextXAlignment = Enum.TextXAlignment.Center, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = RBox, CornerRadius = UDim.new(0,6)})
                    local RStroke = _0xd5fe._0x36b7("UIStroke", {Parent = RBox, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    local GBox = _0xd5fe._0x36b7("TextBox", {Parent = Picker, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Position = UDim2.new(0,206,0,226), Size = UDim2.new(0,30,0,30), Text = "255", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 12, BorderSizePixel = 0, TextXAlignment = Enum.TextXAlignment.Center, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = GBox, CornerRadius = UDim.new(0,6)})
                    local GStroke = _0xd5fe._0x36b7("UIStroke", {Parent = GBox, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    local BBox = _0xd5fe._0x36b7("TextBox", {Parent = Picker, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Position = UDim2.new(0,240,0,226), Size = UDim2.new(0,30,0,30), Text = "255", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 12, BorderSizePixel = 0, TextXAlignment = Enum.TextXAlignment.Center, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = BBox, CornerRadius = UDim.new(0,6)})
                    local BStroke = _0xd5fe._0x36b7("UIStroke", {Parent = BBox, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    
                    RBox.Focused:Connect(function() _0xd5fe._0xa4bd:Create(RStroke, TweenInfo.new(0.15), {Color = Color3.fromRGB(255,100,100)}):Play() end)
                    RBox.FocusLost:Connect(function() _0xd5fe._0xa4bd:Create(RStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() end)
                    GBox.Focused:Connect(function() _0xd5fe._0xa4bd:Create(GStroke, TweenInfo.new(0.15), {Color = Color3.fromRGB(100,255,100)}):Play() end)
                    GBox.FocusLost:Connect(function() _0xd5fe._0xa4bd:Create(GStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() end)
                    BBox.Focused:Connect(function() _0xd5fe._0xa4bd:Create(BStroke, TweenInfo.new(0.15), {Color = Color3.fromRGB(100,100,255)}):Play() end)
                    BBox.FocusLost:Connect(function() _0xd5fe._0xa4bd:Create(BStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() end)
                    
                    local ApplyBtn = _0xd5fe._0x36b7("TextButton", {Parent = Picker, Text = "Apply", Position = UDim2.new(0,12,1,-40), Size = UDim2.new(0.5,-18,0,32), BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor, Font = _0xd5fe._0x0e5f.FontBold, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, BorderSizePixel = 0, AutoButtonColor = false, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = ApplyBtn, CornerRadius = UDim.new(0,6)})
                    ApplyBtn.MouseEnter:Connect(function() _0xd5fe._0xa4bd:Create(ApplyBtn, TweenInfo.new(0.15), {BackgroundColor3 = Color3.new(math.min(1, _0xd5fe._0x0e5f.AccentColor.R+0.1), math.min(1, _0xd5fe._0x0e5f.AccentColor.G+0.1), math.min(1, _0xd5fe._0x0e5f.AccentColor.B+0.1))}):Play() end)
                    ApplyBtn.MouseLeave:Connect(function() _0xd5fe._0xa4bd:Create(ApplyBtn, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play() end)
                    
                    local ResetBtn = _0xd5fe._0x36b7("TextButton", {Parent = Picker, Text = "Reset", Position = UDim2.new(0.5,6,1,-40), Size = UDim2.new(0.5,-18,0,32), BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Font = _0xd5fe._0x0e5f.FontBold, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, BorderSizePixel = 0, AutoButtonColor = false, ZIndex = 101})
                    _0xd5fe._0x36b7("UICorner", {Parent = ResetBtn, CornerRadius = UDim.new(0,6)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = ResetBtn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    ResetBtn.MouseEnter:Connect(function() _0xd5fe._0xa4bd:Create(ResetBtn, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Outline}):Play() end)
                    ResetBtn.MouseLeave:Connect(function() _0xd5fe._0xa4bd:Create(ResetBtn, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element}):Play() end)
                    
                    local function ColorToHex(color)
                        return string.format("#%02X%02X%02X", math.floor(color.R*255), math.floor(color.G*255), math.floor(color.B*255))
                    end
                    
                    local function HexToColor(hex)
                        hex = hex:gsub("#", "")
                        if #hex == 6 then
                            local r = tonumber(hex:sub(1,2), 16) or 255
                            local g = tonumber(hex:sub(3,4), 16) or 255
                            local b = tonumber(hex:sub(5,6), 16) or 255
                            return Color3.fromRGB(r, g, b)
                        end
                        return nil
                    end
                    
                    local function UpdateColor(updateInputs)
                        local col = Color3.fromHSV(CurrentColor.H, CurrentColor.S, CurrentColor.V)
                        ColorBtn.BackgroundColor3 = col
                        SVPicker.BackgroundColor3 = Color3.fromHSV(CurrentColor.H, 1, 1)
                        Preview.BackgroundColor3 = col
                        SVCursor.Position = UDim2.new(CurrentColor.S, 0, 1 - CurrentColor.V, 0)
                        HueCursor.Position = UDim2.new(CurrentColor.H, 0, 0.5, 0)
                        if updateInputs ~= false then
                            HexBox.Text = ColorToHex(col)
                            RBox.Text = tostring(math.floor(col.R * 255))
                            GBox.Text = tostring(math.floor(col.G * 255))
                            BBox.Text = tostring(math.floor(col.B * 255))
                        end
                        pcall(Callback, col)
                    end
                    UpdateColor()
                    
                    HexBox.FocusLost:Connect(function(enter)
                        if enter then
                            local col = HexToColor(HexBox.Text)
                            if col then
                                CurrentColor.H, CurrentColor.S, CurrentColor.V = RGBToHSV(col)
                                UpdateColor()
                            else
                                UpdateColor()
                            end
                        end
                    end)
                    
                    local function UpdateFromRGB()
                        local r = math.clamp(tonumber(RBox.Text) or 0, 0, 255)
                        local g = math.clamp(tonumber(GBox.Text) or 0, 0, 255)
                        local b = math.clamp(tonumber(BBox.Text) or 0, 0, 255)
                        local col = Color3.fromRGB(r, g, b)
                        CurrentColor.H, CurrentColor.S, CurrentColor.V = RGBToHSV(col)
                        UpdateColor(false)
                        HexBox.Text = ColorToHex(col)
                    end
                    RBox.FocusLost:Connect(function(e) if e then UpdateFromRGB() end end)
                    GBox.FocusLost:Connect(function(e) if e then UpdateFromRGB() end end)
                    BBox.FocusLost:Connect(function(e) if e then UpdateFromRGB() end end)
                    
                    local SVDragging = false
                    SVPicker.InputBegan:Connect(function(input)
                        if input.UserInputType == Enum.UserInputType.MouseButton1 then
                            SVDragging = true
                            local inputPos = Vector2.new(input.Position.X, input.Position.Y)
                            local pos = (inputPos - SVPicker.AbsolutePosition) / SVPicker.AbsoluteSize
                            CurrentColor.S = math.clamp(pos.X, 0, 1)
                            CurrentColor.V = math.clamp(1 - pos.Y, 0, 1)
                            UpdateColor()
                        end
                    end)
                    local svConn = _0xd5fe._0x8efd.InputChanged:Connect(function(input)
                        if SVDragging and input.UserInputType == Enum.UserInputType.MouseMovement then
                            local inputPos = Vector2.new(input.Position.X, input.Position.Y)
                            local pos = (inputPos - SVPicker.AbsolutePosition) / SVPicker.AbsoluteSize
                            CurrentColor.S = math.clamp(pos.X, 0, 1)
                            CurrentColor.V = math.clamp(1 - pos.Y, 0, 1)
                            UpdateColor()
                        end
                    end)
                    
                    local HueDragging = false
                    HuePicker.InputBegan:Connect(function(input)
                        if input.UserInputType == Enum.UserInputType.MouseButton1 then
                            HueDragging = true
                            local pos = (input.Position.X - HuePicker.AbsolutePosition.X) / HuePicker.AbsoluteSize.X
                            CurrentColor.H = math.clamp(pos, 0, 1)
                            UpdateColor()
                        end
                    end)
                    local hueConn = _0xd5fe._0x8efd.InputChanged:Connect(function(input)
                        if HueDragging and input.UserInputType == Enum.UserInputType.MouseMovement then
                            local pos = (input.Position.X - HuePicker.AbsolutePosition.X) / HuePicker.AbsoluteSize.X
                            CurrentColor.H = math.clamp(pos, 0, 1)
                            UpdateColor()
                        end
                    end)
                    
                    local endConn = _0xd5fe._0x8efd.InputEnded:Connect(function(input)
                        if input.UserInputType == Enum.UserInputType.MouseButton1 then
                            SVDragging = false
                            HueDragging = false
                        end
                    end)
                    
                    ApplyBtn.MouseButton1Click:Connect(function() Picker:Destroy() ActivePicker = nil end)
                    ResetBtn.MouseButton1Click:Connect(function()
                        CurrentColor.H, CurrentColor.S, CurrentColor.V = RGBToHSV(Default or Color3.new(1,1,1))
                        UpdateColor()
                    end)
                    
                    Picker.Destroying:Connect(function()
                        if svConn then svConn:Disconnect() end
                        if hueConn then hueConn:Disconnect() end
                        if endConn then endConn:Disconnect() end
                    end)
                end)
                
                local ColorPickerObj = {
                    Type = "ColorPicker",
                    Value = Default or Color3.new(1,1,1),
                    Set = function(self, color)
                        ColorBtn.BackgroundColor3 = color
                        CurrentColor.H, CurrentColor.S, CurrentColor.V = RGBToHSV(color)
                        self.Value = color
                        pcall(Callback, color)
                    end,
                    Get = function(self) return Color3.fromHSV(CurrentColor.H, CurrentColor.S, CurrentColor.V) end
                }
                _0xd5fe._0x0e5f.Options[Text] = ColorPickerObj
                return ColorPickerObj
            end
            
            function Group:AddKeybind(Text, Default, Callback)
                local Frame = _0xd5fe._0x36b7("Frame", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,26)})
                local Label = _0xd5fe._0x36b7("TextLabel", {Parent = Frame, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(1,-75,1,0), BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, TextSize = 13})
                
                local Btn = _0xd5fe._0x36b7("TextButton", {Parent = Frame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Size = UDim2.new(0,70,0,22), Position = UDim2.new(1,-70,0,2), Text = (Default and Default.Name) or "None", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 11, AutoButtonColor = false, BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = Btn, CornerRadius = UDim.new(0,5)})
                local BtnStroke = _0xd5fe._0x36b7("UIStroke", {Parent = Btn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                local KeybindObj = {
                    Type = "Keybind",
                    Value = Default,
                    Set = function(self, key)
                        self.Value = key
                        Btn.Text = key and key.Name or "None"
                        -- Update _0xd5fe._0x0e5f.ToggleKey if this is the menu toggle keybind
                        if Text:lower():find("toggle") or Text:lower():find("menu") then
                            _0xd5fe._0x0e5f.ToggleKey = key
                        end
                        pcall(Callback, key)
                    end
                }
                
                Btn.MouseEnter:Connect(function() 
                    _0xd5fe._0xa4bd:Create(BtnStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play()
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.Text}):Play()
                end)
                Btn.MouseLeave:Connect(function() 
                    _0xd5fe._0xa4bd:Create(BtnStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play()
                    _0xd5fe._0xa4bd:Create(Label, TweenInfo.new(0.15), {TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim}):Play()
                end)
                
                Btn.MouseButton1Click:Connect(function()
                    -- Create modal overlay with dark purple tint
                    local Modal = _0xd5fe._0x36b7("Frame", {
                        Parent = ScreenGui,
                        BackgroundColor3 = Color3.fromRGB(30, 20, 50),
                        BackgroundTransparency = 0.3,
                        Size = UDim2.new(1, 0, 1, 0),
                        ZIndex = 5000
                    })
                    
                    local ModalBox = _0xd5fe._0x36b7("Frame", {
                        Parent = Modal,
                        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section,
                        Position = UDim2.new(0.5, 0, 0.5, 0),
                        AnchorPoint = Vector2.new(0.5, 0.5),
                        Size = UDim2.new(0, 280, 0, 140),
                        ZIndex = 5001
                    })
                    _0xd5fe._0x36b7("UICorner", {Parent = ModalBox, CornerRadius = UDim.new(0, 8)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = ModalBox, Color = _0xd5fe._0x0e5f.AccentColor, Thickness = 2})
                    
                    local ModalTitle = _0xd5fe._0x36b7("TextLabel", {
                        Parent = ModalBox,
                        BackgroundTransparency = 1,
                        Position = UDim2.new(0, 0, 0, 15),
                        Size = UDim2.new(1, 0, 0, 25),
                        Text = "Please Press Your Keybind",
                        Font = _0xd5fe._0x0e5f.FontBold,
                        TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
                        TextSize = 16,
                        ZIndex = 5002
                    })
                    
                    local ModalStatus = _0xd5fe._0x36b7("TextLabel", {
                        Parent = ModalBox,
                        BackgroundTransparency = 1,
                        Position = UDim2.new(0, 0, 0, 45),
                        Size = UDim2.new(1, 0, 0, 20),
                        Text = "Waiting for input...",
                        Font = _0xd5fe._0x0e5f.Font,
                        TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
                        TextSize = 14,
                        ZIndex = 5002
                    })
                    
                    local ButtonContainer = _0xd5fe._0x36b7("Frame", {
                        Parent = ModalBox,
                        BackgroundTransparency = 1,
                        Position = UDim2.new(0, 20, 1, -50),
                        Size = UDim2.new(1, -40, 0, 35),
                        ZIndex = 5002,
                        Visible = false
                    })
                    
                    local SaveBtn = _0xd5fe._0x36b7("TextButton", {
                        Parent = ButtonContainer,
                        BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor,
                        Position = UDim2.new(0, 0, 0, 0),
                        Size = UDim2.new(0.48, 0, 1, 0),
                        Text = "Save",
                        Font = _0xd5fe._0x0e5f.FontBold,
                        TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
                        TextSize = 14,
                        AutoButtonColor = false,
                        ZIndex = 5003
                    })
                    _0xd5fe._0x36b7("UICorner", {Parent = SaveBtn, CornerRadius = UDim.new(0, 6)})
                    
                    local ResetBtn = _0xd5fe._0x36b7("TextButton", {
                        Parent = ButtonContainer,
                        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element,
                        Position = UDim2.new(0.52, 0, 0, 0),
                        Size = UDim2.new(0.48, 0, 1, 0),
                        Text = "Reset",
                        Font = _0xd5fe._0x0e5f.FontBold,
                        TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
                        TextSize = 14,
                        AutoButtonColor = false,
                        ZIndex = 5003
                    })
                    _0xd5fe._0x36b7("UICorner", {Parent = ResetBtn, CornerRadius = UDim.new(0, 6)})
                    _0xd5fe._0x36b7("UIStroke", {Parent = ResetBtn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                    
                    local pendingKey = nil
                    local con
                    con = _0xd5fe._0x8efd.InputBegan:Connect(function(input)
                        if input.UserInputType == Enum.UserInputType.Keyboard then
                            local key = input.KeyCode
                            if key == Enum.KeyCode.Unknown or key == Enum.KeyCode.Escape then 
                                Modal:Destroy()
                                con:Disconnect()
                                return 
                            end
                            pendingKey = key
                            ModalTitle.Text = "Keybind Set to " .. key.Name
                            ModalStatus.Text = "Press Save to confirm or Reset to remove"
                            ModalStatus.TextColor3 = _0xd5fe._0x0e5f.AccentColor
                            ButtonContainer.Visible = true
                            con:Disconnect()
                        end
                    end)
                    
                    SaveBtn.MouseButton1Click:Connect(function()
                        if pendingKey then
                            KeybindObj.Value = pendingKey
                            Btn.Text = pendingKey.Name
                            if Text:lower():find("toggle") or Text:lower():find("menu") then
                                _0xd5fe._0x0e5f.ToggleKey = pendingKey
                            end
                            pcall(Callback, pendingKey)
                        end
                        Modal:Destroy()
                    end)
                    
                    ResetBtn.MouseButton1Click:Connect(function()
                        KeybindObj.Value = nil
                        Btn.Text = "None"
                        if Text:lower():find("toggle") or Text:lower():find("menu") then
                            _0xd5fe._0x0e5f.ToggleKey = nil
                        end
                        pcall(Callback, nil)
                        Modal:Destroy()
                    end)
                    
                    SaveBtn.MouseEnter:Connect(function()
                        _0xd5fe._0xa4bd:Create(SaveBtn, TweenInfo.new(0.15), {BackgroundColor3 = Color3.fromRGB(116, 96, 255)}):Play()
                    end)
                    SaveBtn.MouseLeave:Connect(function()
                        _0xd5fe._0xa4bd:Create(SaveBtn, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
                    end)
                    ResetBtn.MouseEnter:Connect(function()
                        _0xd5fe._0xa4bd:Create(ResetBtn, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Error}):Play()
                    end)
                    ResetBtn.MouseLeave:Connect(function()
                        _0xd5fe._0xa4bd:Create(ResetBtn, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element}):Play()
                    end)
                end)
                
                -- Set initial toggle key if this is the menu toggle keybind
                if (Text:lower():find("toggle") or Text:lower():find("menu")) and Default then
                    _0xd5fe._0x0e5f.ToggleKey = Default
                end
                
                _0xd5fe._0x0e5f.Options[Text] = KeybindObj
                return KeybindObj
            end
            
            function Group:AddButton(Text, Callback)
                local Btn = _0xd5fe._0x36b7("TextButton", {Parent = Container, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Size = UDim2.new(1,0,0,30), Text = Text, Font = _0xd5fe._0x0e5f.FontBold, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, AutoButtonColor = false, BorderSizePixel = 0})
                _0xd5fe._0x36b7("UICorner", {Parent = Btn, CornerRadius = UDim.new(0,6)})
                _0xd5fe._0x36b7("UIStroke", {Parent = Btn, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                
                Btn.MouseEnter:Connect(function() _0xd5fe._0xa4bd:Create(Btn, TweenInfo.new(0.2), {BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play() end)
                Btn.MouseLeave:Connect(function() _0xd5fe._0xa4bd:Create(Btn, TweenInfo.new(0.2), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element}):Play() end)
                Btn.MouseButton1Click:Connect(function() pcall(Callback) end)
            end
            
            function Group:AddInput(Text, Placeholder, Callback)
                local Frame = _0xd5fe._0x36b7("Frame", {Parent = Container, BackgroundTransparency = 1, Size = UDim2.new(1,0,0,50)})
                _0xd5fe._0x36b7("TextLabel", {Parent = Frame, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(1,0,0,18), BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, TextSize = 13})
                
                local Box = _0xd5fe._0x36b7("TextBox", {Parent = Frame, BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element, Position = UDim2.new(0,0,0,22), Size = UDim2.new(1,0,0,26), PlaceholderText = Placeholder or "", Text = "", Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.Text, TextSize = 13, TextXAlignment = Enum.TextXAlignment.Left, BorderSizePixel = 0, ClearTextOnFocus = false})
                _0xd5fe._0x36b7("UICorner", {Parent = Box, CornerRadius = UDim.new(0,6)})
                local InputStroke = _0xd5fe._0x36b7("UIStroke", {Parent = Box, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
                _0xd5fe._0x36b7("UIPadding", {Parent = Box, PaddingLeft = UDim.new(0,10)})
                
                local InputObj = {
                    Type = "Input",
                    Value = "",
                    Set = function(self, text)
                        Box.Text = text
                        self.Value = text
                        pcall(Callback, text)
                    end
                }
                
                Box.Focused:Connect(function() _0xd5fe._0xa4bd:Create(InputStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.AccentColor}):Play() end)
                Box.FocusLost:Connect(function(enter) 
                    _0xd5fe._0xa4bd:Create(InputStroke, TweenInfo.new(0.15), {Color = _0xd5fe._0x0e5f.Theme.Outline}):Play() 
                    InputObj.Value = Box.Text
                    if enter then pcall(Callback, Box.Text) end 
                end)
                
                _0xd5fe._0x0e5f.Options[Text] = InputObj
                return InputObj
            end
            
            function Group:AddLabel(Text)
                local Lbl = _0xd5fe._0x36b7("TextLabel", {Parent = Container, Text = Text, Font = _0xd5fe._0x0e5f.Font, TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim, Size = UDim2.new(1,0,0,18), BackgroundTransparency = 1, TextXAlignment = Enum.TextXAlignment.Left, TextSize = 13, TextWrapped = true})
                return {Set = function(self, txt) Lbl.Text = txt end}
            end
            
            return Group
        end
        
        function Tab:AddLeftGroupbox(Name) return self:CreateGroupbox(Left, Name) end
        function Tab:AddRightGroupbox(Name) return self:CreateGroupbox(Right, Name) end
        
        return Tab
    end
    
    return WindowObj
end

-- Config Manager System (Fluent-style)
local HttpService = game:GetService("HttpService")

_0xd5fe._0x0e5f.Options = {}

_0xd5fe._0x0e5f.SaveManager = {
    Folder = "UILibraryConfigs",
    Ignore = {},
    Parser = {
        Toggle = {
            Save = function(idx, object)
                return { type = "Toggle", idx = idx, value = object.Value }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set then
                    _0xd5fe._0x0e5f.Options[idx]:Set(data.value)
                end
            end
        },
        Slider = {
            Save = function(idx, object)
                return { type = "Slider", idx = idx, value = object.Value }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set then
                    _0xd5fe._0x0e5f.Options[idx]:Set(data.value)
                end
            end
        },
        Dropdown = {
            Save = function(idx, object)
                return { type = "Dropdown", idx = idx, value = object.Value }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set then
                    _0xd5fe._0x0e5f.Options[idx]:Set(data.value)
                end
            end
        },
        ColorPicker = {
            Save = function(idx, object)
                local c = object.Value
                return { type = "ColorPicker", idx = idx, value = {c.R, c.G, c.B} }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set then
                    _0xd5fe._0x0e5f.Options[idx]:Set(Color3.new(data.value[1], data.value[2], data.value[3]))
                end
            end
        },
        Keybind = {
            Save = function(idx, object)
                return { type = "Keybind", idx = idx, value = object.Value and object.Value.Name or "None" }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set and data.value ~= "None" then
                    _0xd5fe._0x0e5f.Options[idx]:Set(Enum.KeyCode[data.value])
                end
            end
        },
        Input = {
            Save = function(idx, object)
                return { type = "Input", idx = idx, value = object.Value }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set then
                    _0xd5fe._0x0e5f.Options[idx]:Set(data.value)
                end
            end
        },
        MultiDropdown = {
            Save = function(idx, object)
                -- Convert the dictionary {["opt1"] = true, ["opt2"] = true} to array {"opt1", "opt2"}
                local selectedArray = {}
                if type(object.Value) == "table" then
                    for opt, isSelected in pairs(object.Value) do
                        if isSelected then
                            table.insert(selectedArray, opt)
                        end
                    end
                end
                return { type = "MultiDropdown", idx = idx, value = selectedArray }
            end,
            Load = function(idx, data)
                if _0xd5fe._0x0e5f.Options[idx] and _0xd5fe._0x0e5f.Options[idx].Set then
                    -- data.value is already an array, Set expects an array
                    _0xd5fe._0x0e5f.Options[idx]:Set(data.value or {})
                end
            end
        }
    }
}

function _0xd5fe._0x0e5f.SaveManager:SetIgnoreIndexes(list)
    for _, key in next, list do
        self.Ignore[key] = true
    end
end

function _0xd5fe._0x0e5f.SaveManager:SetFolder(folder)
    self.Folder = folder
    self:BuildFolderTree()
end

function _0xd5fe._0x0e5f.SaveManager:BuildFolderTree()
    local paths = { self.Folder, self.Folder .. "/settings" }
    for i = 1, #paths do
        if not isfolder(paths[i]) then
            makefolder(paths[i])
        end
    end
end

function _0xd5fe._0x0e5f.SaveManager:RefreshConfigList()
    local list = listfiles(self.Folder .. "/settings")
    local out = {}
    for i = 1, #list do
        local file = list[i]
        if file:sub(-5) == ".json" then
            local name = file:match("([^/\\]+)%.json$")
            if name and name ~= "autoload" then
                table.insert(out, name)
            end
        end
    end
    return out
end

function _0xd5fe._0x0e5f.SaveManager:Save(name)
    if not name or name:gsub(" ", "") == "" then
        return false, "invalid name"
    end
    
    self:BuildFolderTree()
    local fullPath = self.Folder .. "/settings/" .. name .. ".json"
    
    local data = { objects = {} }
    
    for idx, option in next, _0xd5fe._0x0e5f.Options do
        if not self.Parser[option.Type] then continue end
        if self.Ignore[idx] then continue end
        table.insert(data.objects, self.Parser[option.Type].Save(idx, option))
    end
    
    local success, encoded = pcall(HttpService.JSONEncode, HttpService, data)
    if not success then
        return false, "encode error"
    end
    
    writefile(fullPath, encoded)
    return true
end

function _0xd5fe._0x0e5f.SaveManager:Load(name)
    if not name or name:gsub(" ", "") == "" then
        return false, "invalid name"
    end
    
    local file = self.Folder .. "/settings/" .. name .. ".json"
    if not isfile(file) then return false, "file not found" end
    
    local success, decoded = pcall(HttpService.JSONDecode, HttpService, readfile(file))
    if not success then return false, "decode error" end
    
    local loadedCount = 0
    
    -- Set loading flag so toggle callbacks can skip side-effects (e.g. safespot teleport)
    _0xd5fe._0x0e5f._isLoadingConfig = true
    
    -- Load order: MultiDropdowns and Dropdowns first, then other settings, Toggles last
    -- This ensures data is populated before toggles fire their callbacks
    local toggles = {}
    local others = {}
    
    for _, option in next, decoded.objects do
        if option.type == "Toggle" then
            table.insert(toggles, option)
        else
            table.insert(others, option)
        end
    end
    
    -- Helper function to load a single option
    local function loadOption(option)
        local idx = option.idx
        local optType = option.type
        local optionObj = _0xd5fe._0x0e5f.Options[idx]
        
        if optionObj and optionObj.Set then
            local ok, err = pcall(function()
                if optType == "Toggle" then
                    optionObj:Set(option.value)
                elseif optType == "Slider" then
                    optionObj:Set(option.value)
                elseif optType == "Dropdown" then
                    optionObj:Set(option.value)
                elseif optType == "ColorPicker" then
                    optionObj:Set(Color3.new(option.value[1], option.value[2], option.value[3]))
                elseif optType == "Keybind" then
                    if option.value ~= "None" then
                        optionObj:Set(Enum.KeyCode[option.value])
                    end
                elseif optType == "Input" then
                    optionObj:Set(option.value)
                elseif optType == "MultiDropdown" then
                    optionObj:Set(option.value or {})
                end
            end)
            if ok then 
                loadedCount = loadedCount + 1 
            else
                warn("Failed to load " .. idx .. ": " .. tostring(err))
            end
        end
    end
    
    -- Load non-toggles first (dropdowns, sliders, inputs, etc.)
    for _, option in ipairs(others) do
        loadOption(option)
    end
    
    -- Small delay to ensure callbacks complete before loading toggles
    task.wait(0.1)
    
    -- Load toggles last so they have access to populated data
    for _, option in ipairs(toggles) do
        loadOption(option)
    end
    
    -- Clear loading flag after all options are loaded
    _0xd5fe._0x0e5f._isLoadingConfig = false
    
    return true, loadedCount
end

function _0xd5fe._0x0e5f.SaveManager:Delete(name)
    local path = self.Folder .. "/settings/" .. name .. ".json"
    if isfile(path) then
        delfile(path)
        return true
    end
    return false
end

function _0xd5fe._0x0e5f.SaveManager:LoadAutoloadConfig()
    local autoloadPath = self.Folder .. "/settings/autoload.txt"
    if isfile(autoloadPath) then
        local name = readfile(autoloadPath)
        if name and name ~= "" then
            local success, count = self:Load(name)
            if success then
                _0xd5fe._0x0e5f:Notify("Config", "Auto-loaded: " .. name .. " (" .. tostring(count or 0) .. " settings)", 3, "folder")
            else
                _0xd5fe._0x0e5f:Notify("Config", "Failed to auto-load: " .. name, 3, "error")
            end
            return true
        end
    end
    return false
end

function _0xd5fe._0x0e5f.SaveManager:GetAutoloadName()
    local autoloadPath = self.Folder .. "/settings/autoload.txt"
    if isfile(autoloadPath) then
        local name = readfile(autoloadPath)
        if name and name ~= "" then
            return name
        end
    end
    return "None"
end

function _0xd5fe._0x0e5f.SaveManager:BuildConfigSection(tab)
    local ConfigGroup = tab:AddRightGroupbox("Configuration")
    
    local configNameValue = ""
    local selectedConfig = ""
    
    -- Current Auto Load label
    local autoloadLabel = ConfigGroup:AddLabel("Current Auto Load: " .. self:GetAutoloadName())
    
    ConfigGroup:AddInput("SaveManager_ConfigName", "Config name...", function(text)
        configNameValue = text
    end)
    
    local configList = self:RefreshConfigList()
    local dropdownRef = nil
    
    dropdownRef = ConfigGroup:AddDropdown("SaveManager_ConfigList", configList, nil, function(opt)
        selectedConfig = opt or ""
    end)
    
    ConfigGroup:AddButton("Create Config", function()
        local name = configNameValue
        if not name or name:gsub(" ", "") == "" then
            return _0xd5fe._0x0e5f:Notify("Config", "Enter a config name", 3, "error")
        end
        
        local success, err = self:Save(name)
        if not success then
            return _0xd5fe._0x0e5f:Notify("Config", "Failed to save: " .. (err or "unknown"), 3, "error")
        end
        
        _0xd5fe._0x0e5f:Notify("Config", "Created: " .. name, 3, "folder")
        
        if dropdownRef and dropdownRef.Refresh then
            dropdownRef:Refresh(self:RefreshConfigList())
        end
    end)
    
    ConfigGroup:AddButton("Load Config", function()
        if not selectedConfig or selectedConfig == "" then
            return _0xd5fe._0x0e5f:Notify("Config", "Select a config first", 3, "error")
        end
        
        local success, err = self:Load(selectedConfig)
        if not success then
            return _0xd5fe._0x0e5f:Notify("Config", "Failed to load: " .. (err or "unknown"), 3, "error")
        end
        
        _0xd5fe._0x0e5f:Notify("Config", "Loaded: " .. selectedConfig, 3, "folder")
    end)
    
    ConfigGroup:AddButton("Overwrite Config", function()
        if not selectedConfig or selectedConfig == "" then
            return _0xd5fe._0x0e5f:Notify("Config", "Select a config first", 3, "error")
        end
        
        local success, err = self:Save(selectedConfig)
        if not success then
            return _0xd5fe._0x0e5f:Notify("Config", "Failed to save: " .. (err or "unknown"), 3, "error")
        end
        
        _0xd5fe._0x0e5f:Notify("Config", "Overwrote: " .. selectedConfig, 3, "folder")
    end)
    
    ConfigGroup:AddButton("Delete Config", function()
        if not selectedConfig or selectedConfig == "" then
            return _0xd5fe._0x0e5f:Notify("Config", "Select a config first", 3, "error")
        end
        
        if self:Delete(selectedConfig) then
            _0xd5fe._0x0e5f:Notify("Config", "Deleted: " .. selectedConfig, 3, "trash")
            selectedConfig = ""
            if dropdownRef and dropdownRef.Refresh then
                dropdownRef:Refresh(self:RefreshConfigList())
            end
        else
            _0xd5fe._0x0e5f:Notify("Config", "Failed to delete", 3, "error")
        end
    end)
    
    ConfigGroup:AddButton("Refresh List", function()
        if dropdownRef and dropdownRef.Refresh then
            dropdownRef:Refresh(self:RefreshConfigList())
        end
        _0xd5fe._0x0e5f:Notify("Config", "Refreshed config list", 2, "refresh")
    end)
    
    ConfigGroup:AddButton("Set as Auto-Load", function()
        if not selectedConfig or selectedConfig == "" then
            return _0xd5fe._0x0e5f:Notify("Config", "Select a config first", 3, "error")
        end
        
        self:BuildFolderTree()
        writefile(self.Folder .. "/settings/autoload.txt", selectedConfig)
        autoloadLabel:Set("Current Auto Load: " .. selectedConfig)
        _0xd5fe._0x0e5f:Notify("Config", "Auto-load set: " .. selectedConfig, 3, "folder")
    end)
    
    self:SetIgnoreIndexes({"SaveManager_ConfigName", "SaveManager_ConfigList"})
end

function _0xd5fe._0x0e5f.SaveManager:BuildCommunityConfigSection(tab, apiUrl)
    local CommunityGroup = tab:AddLeftGroupbox("Community Configs")
    
    local selectedCommunityConfig = nil
    local communityConfigs = {}
    local configEntryFrames = {}
    
    -- HTTP request helper (executor compatibility)
    -- Google Apps Script returns 302 redirects; game:HttpGet follows them automatically
    local function httpGet(url)
        local success, result = pcall(function()
            return game:HttpGet(url)
        end)
        if not success then return nil, tostring(result) end
        return {Body = result}
    end
    
    local function httpPost(url, body)
        local requestFn = (type(request) == "function" and request) 
            or (type(http_request) == "function" and http_request)
            or (type(http) == "table" and http.request)
            or (type(syn) == "table" and syn.request)
            or (type(fluxus) == "table" and fluxus.request)
        if not requestFn then return nil, "No HTTP function available" end
        local success, result = pcall(requestFn, {
            Url = url,
            Method = "POST",
            Headers = {["Content-Type"] = "application/json"},
            Body = body
        })
        if not success then return nil, tostring(result) end
        -- Handle redirects: if status is 302/301, follow the Location header
        if result and result.StatusCode and (result.StatusCode == 302 or result.StatusCode == 301) then
            local location = result.Headers and (result.Headers["Location"] or result.Headers["location"])
            if location then
                return httpGet(location)
            end
        end
        return result
    end
    
    -- Get a unique identifier for like tracking
    local function getHWID()
        local hwid = "unknown"
        pcall(function()
            if type(gethwid) == "function" then
                hwid = gethwid()
            elseif type(getguid) == "function" then
                hwid = getguid()
            else
                hwid = game:GetService("Players").LocalPlayer.UserId .. "_" .. game:GetService("Players").LocalPlayer.Name
            end
        end)
        return hwid
    end
    
    -- Status label
    local statusLabel = CommunityGroup:AddLabel("Status: Not loaded")
    
    -- Build scrollable config list inside the groupbox container
    local ScrollHolder = _0xd5fe._0x36b7("Frame", {
        Parent = CommunityGroup._container,
        BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element,
        Size = UDim2.new(1, 0, 0, 180),
        BorderSizePixel = 0,
        ClipsDescendants = true
    })
    _0xd5fe._0x36b7("UICorner", {Parent = ScrollHolder, CornerRadius = UDim.new(0, 6)})
    _0xd5fe._0x36b7("UIStroke", {Parent = ScrollHolder, Color = _0xd5fe._0x0e5f.Theme.Outline, Thickness = 1})
    
    local ScrollList = _0xd5fe._0x36b7("ScrollingFrame", {
        Parent = ScrollHolder,
        BackgroundTransparency = 1,
        Size = UDim2.new(1, 0, 1, 0),
        BorderSizePixel = 0,
        ScrollBarThickness = 3,
        ScrollBarImageColor3 = _0xd5fe._0x0e5f.AccentColor,
        CanvasSize = UDim2.new(0, 0, 0, 0),
        AutomaticCanvasSize = Enum.AutomaticSize.Y
    })
    _0xd5fe._0x36b7("UIListLayout", {Parent = ScrollList, SortOrder = Enum.SortOrder.LayoutOrder, Padding = UDim.new(0, 2)})
    _0xd5fe._0x36b7("UIPadding", {Parent = ScrollList, PaddingLeft = UDim.new(0, 4), PaddingRight = UDim.new(0, 4), PaddingTop = UDim.new(0, 4), PaddingBottom = UDim.new(0, 4)})
    
    local configEntryStates = {}
    
    local function clearList()
        for _, frame in pairs(configEntryFrames) do
            pcall(function() frame:Destroy() end)
        end
        configEntryFrames = {}
        configEntryStates = {}
        selectedCommunityConfig = nil
    end
    
    local function createConfigEntry(config, index)
        local isSelected = false
        
        -- Parse ISO timestamp to a clean date string (e.g. "04/18/2026")
        local dateStr = ""
        if config.timestamp and config.timestamp ~= "" then
            local y, m, d = string.match(tostring(config.timestamp), "(%d+)-(%d+)-(%d+)")
            if y and m and d then
                dateStr = m .. "/" .. d .. "/" .. y
            end
        end
        
        local Entry = _0xd5fe._0x36b7("TextButton", {
            Parent = ScrollList,
            BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section,
            Size = UDim2.new(1, -4, 0, 40),
            Text = "",
            AutoButtonColor = false,
            BorderSizePixel = 0,
            LayoutOrder = index
        })
        _0xd5fe._0x36b7("UICorner", {Parent = Entry, CornerRadius = UDim.new(0, 5)})
        
        local NameLabel = _0xd5fe._0x36b7("TextLabel", {
            Parent = Entry,
            Text = config.name,
            Font = _0xd5fe._0x0e5f.FontBold,
            TextColor3 = _0xd5fe._0x0e5f.Theme.Text,
            Size = UDim2.new(1, -80, 0, 20),
            Position = UDim2.new(0, 8, 0, 2),
            BackgroundTransparency = 1,
            TextXAlignment = Enum.TextXAlignment.Left,
            TextSize = 12,
            TextTruncate = Enum.TextTruncate.AtEnd,
            Active = false
        })
        
        local DateLabel = _0xd5fe._0x36b7("TextLabel", {
            Parent = Entry,
            Text = dateStr,
            Font = _0xd5fe._0x0e5f.Font,
            TextColor3 = _0xd5fe._0x0e5f.Theme.TextDim,
            Size = UDim2.new(0.5, -8, 0, 16),
            Position = UDim2.new(0, 8, 0, 22),
            BackgroundTransparency = 1,
            TextXAlignment = Enum.TextXAlignment.Left,
            TextSize = 10,
            Active = false
        })
        
        local LikeLabel = _0xd5fe._0x36b7("TextLabel", {
            Parent = Entry,
            Text = "Likes: " .. tostring(config.likes or 0),
            Font = _0xd5fe._0x0e5f.FontBold,
            TextColor3 = Color3.fromRGB(255, 100, 120),
            Size = UDim2.new(0, 70, 0, 16),
            Position = UDim2.new(1, -75, 0, 22),
            BackgroundTransparency = 1,
            TextXAlignment = Enum.TextXAlignment.Right,
            TextSize = 10,
            Active = false
        })
        
        Entry.MouseEnter:Connect(function()
            if not isSelected then
                _0xd5fe._0xa4bd:Create(Entry, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Element}):Play()
            end
        end)
        Entry.MouseLeave:Connect(function()
            if not isSelected then
                _0xd5fe._0xa4bd:Create(Entry, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section}):Play()
            end
        end)
        
        Entry.MouseButton1Click:Connect(function()
            -- Deselect all others
            for i, otherFrame in pairs(configEntryFrames) do
                if configEntryStates[i] then
                    configEntryStates[i].selected = false
                end
                pcall(function()
                    _0xd5fe._0xa4bd:Create(otherFrame, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.Theme.Section}):Play()
                end)
            end
            -- Select this one
            isSelected = true
            selectedCommunityConfig = config
            _0xd5fe._0xa4bd:Create(Entry, TweenInfo.new(0.15), {BackgroundColor3 = _0xd5fe._0x0e5f.AccentColor}):Play()
            statusLabel:Set("Selected: " .. config.name)
        end)
        
        table.insert(configEntryFrames, Entry)
        configEntryStates[#configEntryFrames] = {selected = false, config = config, likeLabel = LikeLabel}
    end
    
    local function refreshList()
        statusLabel:Set("Status: Loading...")
        
        task.spawn(function()
            local response, err = httpGet(apiUrl .. "?action=list")
            
            if not response then
                statusLabel:Set("ERR: No response")
                return
            end
            
            if not response.Body then
                statusLabel:Set("ERR: Empty body")
                return
            end
            
            local success, data = pcall(function()
                return _0xd5fe._0x740e:JSONDecode(response.Body)
            end)
            
            if not success then
                statusLabel:Set("ERR: JSON parse fail")
                return
            end
            
            if not data or not data.success then
                statusLabel:Set("ERR: " .. (data and data.error or "Unknown API error"))
                return
            end
            
            communityConfigs = data.configs or {}
            clearList()
            
            for i, config in ipairs(communityConfigs) do
                createConfigEntry(config, i)
            end
            
            statusLabel:Set("Status: " .. #communityConfigs .. " configs loaded")
        end)
    end
    
    -- Dropdown of local configs for upload
    local selectedUploadConfig = ""
    local localConfigList = self:RefreshConfigList()
    local uploadDropdownRef = nil
    
    uploadDropdownRef = CommunityGroup:AddDropdown("CC_UploadSelect", localConfigList, nil, function(opt)
        selectedUploadConfig = opt or ""
    end)
    
    CommunityGroup:AddButton("Save Selected", function()
        if not selectedCommunityConfig then
            return _0xd5fe._0x0e5f:Notify("Community", "Select a config from the list first", 3, "error")
        end
        
        local configData = selectedCommunityConfig.data
        if not configData or configData == "" then
            return _0xd5fe._0x0e5f:Notify("Community", "Config has no data", 3, "error")
        end
        
        -- Save the community config as a local .json file
        local saveName = selectedCommunityConfig.name
        local filePath = self.Folder .. "/settings/" .. saveName .. ".json"
        
        local ok, writeErr = pcall(function()
            writefile(filePath, configData)
        end)
        
        if not ok then
            return _0xd5fe._0x0e5f:Notify("Community", "Failed to save: " .. tostring(writeErr), 3, "error")
        end
        
        _0xd5fe._0x0e5f:Notify("Community", "Saved '" .. saveName .. "' to your configs!", 3, "check")
        
        -- Refresh the SaveManager config list and upload dropdown so it appears
        if _0xd5fe._0x0e5f.Options["SaveManager_ConfigList"] then
            _0xd5fe._0x0e5f.Options["SaveManager_ConfigList"]:Refresh(self:RefreshConfigList())
        end
        if uploadDropdownRef and uploadDropdownRef.Refresh then
            uploadDropdownRef:Refresh(self:RefreshConfigList())
        end
    end)
    
    CommunityGroup:AddButton("Upload Selected Config", function()
        if not selectedUploadConfig or selectedUploadConfig == "" then
            return _0xd5fe._0x0e5f:Notify("Community", "Select a local config first", 3, "error")
        end
        
        -- Read the actual saved config file from disk
        local filePath = self.Folder .. "/settings/" .. selectedUploadConfig .. ".json"
        if not isfile(filePath) then
            return _0xd5fe._0x0e5f:Notify("Community", "Config file not found", 3, "error")
        end
        
        local configJson = readfile(filePath)
        local author = game:GetService("Players").LocalPlayer.Name
        
        _0xd5fe._0x0e5f:Notify("Community", "Uploading...", 2, "info")
        
        task.spawn(function()
            local response, err = httpPost(apiUrl, _0xd5fe._0x740e:JSONEncode({
                    action = "upload",
                    name = selectedUploadConfig,
                    author = author,
                    data = configJson
                }))
            
            if not response or not response.Body then
                _0xd5fe._0x0e5f:Notify("Community", "Upload failed: " .. (err or "No response"), 3, "error")
                return
            end
            
            local success, data = pcall(function()
                return _0xd5fe._0x740e:JSONDecode(response.Body)
            end)
            
            if success and data and data.success then
                _0xd5fe._0x0e5f:Notify("Community", "Uploaded: " .. selectedUploadConfig, 3, "check")
                refreshList()
            else
                _0xd5fe._0x0e5f:Notify("Community", "Upload failed: " .. (data and data.error or "Unknown error"), 3, "error")
            end
        end)
    end)
    
    CommunityGroup:AddButton("Like Selected", function()
        if not selectedCommunityConfig then
            return _0xd5fe._0x0e5f:Notify("Community", "Select a config from the list first", 3, "error")
        end
        
        local configToLike = selectedCommunityConfig
        local hwid = getHWID()
        
        task.spawn(function()
            local response, err = httpPost(apiUrl, _0xd5fe._0x740e:JSONEncode({
                    action = "like",
                    id = configToLike.id,
                    hwid = hwid
                }))
            
            if not response or not response.Body then
                _0xd5fe._0x0e5f:Notify("Community", "Like failed", 3, "error")
                return
            end
            
            local success, data = pcall(function()
                return _0xd5fe._0x740e:JSONDecode(response.Body)
            end)
            
            if success and data and data.success then
                local msg = data.liked and "Liked!" or "Unliked!"
                _0xd5fe._0x0e5f:Notify("Community", msg .. " (" .. (data.likes or 0) .. " total)", 3, "check")
                refreshList()
            else
                _0xd5fe._0x0e5f:Notify("Community", "Like failed: " .. (data and data.error or "Unknown"), 3, "error")
            end
        end)
    end)
    
    CommunityGroup:AddButton("Delete My Config", function()
        if not selectedUploadConfig or selectedUploadConfig == "" then
            return _0xd5fe._0x0e5f:Notify("Community", "Select your config from the upload dropdown first", 3, "error")
        end
        
        local author = game:GetService("Players").LocalPlayer.Name
        
        -- Find the matching cloud config by name and author
        local matchedConfig = nil
        for _, cfg in ipairs(communityConfigs) do
            if cfg.name == selectedUploadConfig and cfg.author == author then
                matchedConfig = cfg
                break
            end
        end
        
        if not matchedConfig then
            return _0xd5fe._0x0e5f:Notify("Community", "'" .. selectedUploadConfig .. "' is not uploaded or not yours", 3, "error")
        end
        
        task.spawn(function()
            local response, err = httpPost(apiUrl, _0xd5fe._0x740e:JSONEncode({
                    action = "delete",
                    id = matchedConfig.id,
                    author = author
                }))
            
            if not response or not response.Body then
                _0xd5fe._0x0e5f:Notify("Community", "Delete failed", 3, "error")
                return
            end
            
            local success, data = pcall(function()
                return _0xd5fe._0x740e:JSONDecode(response.Body)
            end)
            
            if success and data and data.success then
                _0xd5fe._0x0e5f:Notify("Community", "Deleted '" .. selectedUploadConfig .. "' from cloud!", 3, "check")
                refreshList()
            else
                _0xd5fe._0x0e5f:Notify("Community", "Delete failed: " .. (data and data.error or "Unknown"), 3, "error")
            end
        end)
    end)
    
    CommunityGroup:AddButton("Refresh", function()
        refreshList()
        if uploadDropdownRef and uploadDropdownRef.Refresh then
            uploadDropdownRef:Refresh(self:RefreshConfigList())
        end
    end)
    
    -- Ignore community config UI elements from being saved
    self:SetIgnoreIndexes({"CC_UploadSelect"})
    
    -- Auto-load on build
    task.spawn(function()
        task.wait(2)
        refreshList()
    end)
end

_0xd5fe._0x0e5f.SaveManager:BuildFolderTree()

return _0xd5fe._0x0e5f
