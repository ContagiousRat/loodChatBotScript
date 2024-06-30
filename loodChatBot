-- Create ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Create Frame
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 300, 0, 215)
frame.Position = UDim2.new(0.5, -150, 0.5, -90)
frame.BackgroundColor3 = Color3.new(1, 1, 1)
frame.Active = true
frame.Draggable = true
frame.Parent = screenGui

-- Create Label for TextBox1
local label1 = Instance.new("TextLabel")
label1.Size = UDim2.new(0, 260, 0, 20)
label1.Position = UDim2.new(0, 20, 0, 10)
label1.BackgroundColor3 = Color3.new(0.8, 0.8, 0.8)
label1.Text = "Enter your question here:"
label1.Parent = frame

-- Create TextBox1 for user input
local textBox1 = Instance.new("TextBox")
textBox1.Size = UDim2.new(0, 260, 0, 60)
textBox1.Position = UDim2.new(0, 20, 0, 40)
textBox1.BackgroundColor3 = Color3.new(1, 1, 1)
textBox1.PlaceholderText = "Type here..."
textBox1.TextWrapped = true
textBox1.ClearTextOnFocus = false
textBox1.MultiLine = true
textBox1.Parent = frame

-- Create Button to send the message inside the TextBox1
local button = Instance.new("TextButton")
button.Size = UDim2.new(0, 20, 0, 20)
button.Position = UDim2.new(1, -30, 1, -30)
button.BackgroundColor3 = Color3.new(0, 1, 0)
button.Text = ""
button.Parent = textBox1

-- Create Label for TextBox2
local label2 = Instance.new("TextLabel")
label2.Size = UDim2.new(0, 260, 0, 20)
label2.Position = UDim2.new(0, 20, 0, 110)
label2.BackgroundColor3 = Color3.new(0.8, 0.8, 0.8)
label2.Text = "Response:"
label2.Parent = frame

-- Create TextBox2 for bot response
local textBox2 = Instance.new("TextBox")
textBox2.Size = UDim2.new(0, 260, 0, 60)
textBox2.Position = UDim2.new(0, 20, 0, 140)
textBox2.BackgroundColor3 = Color3.new(1, 1, 1)
textBox2.PlaceholderText = "The response will appear here..."
textBox2.TextWrapped = true
textBox2.ClearTextOnFocus = false
textBox2.MultiLine = true
textBox2.TextEditable = false
textBox2.Parent = frame

-- Function to generate a response
local function getBotResponse(userInput)
    local responses = {
        ["hello"] = "Hello! How can I assist you today?",
        ["hi"] = "Hi there! What can I do for you?",
        ["how are you"] = "I'm just a script, but I'm here to help!",
        ["what is your name"] = "I'm your friendly Roblox chatbot!",
        ["bye"] = "Goodbye! Have a great day!",
        ["what is roblox"] = "Roblox is an online platform that allows users to create and play games created by other users.",
        ["who made you"] = "I was created by a Roblox developer!",
        ["what can you do"] = "I can chat with you and answer simple questions!",
        ["help"] = "Sure, I'm here to help! Ask me anything.",
        ["thanks"] = "You're welcome! Anything else?",
        ["what is lua"] = "Lua is a lightweight, high-level programming language commonly used in game development.",
        ["tell me a joke"] = "Why don't scientists trust atoms? Because they make up everything!",
        ["what's your favorite game"] = "I'm just a script, but I've heard Adopt Me is popular!",
        ["how old are you"] = "I'm as old as the code running me!",
        ["where are you from"] = "I live in the digital world of Roblox!",
        ["what's the weather"] = "I'm not sure, but it looks clear inside Roblox Studio!",
        ["who is your creator"] = "I was created by a developer in Roblox Studio.",
        ["can you dance"] = "I'm just a script, so I can't dance, but you can dance in Roblox!",
        ["what's your favorite color"] = "I like all the colors in the RGB spectrum!",
        ["what is your purpose"] = "My purpose is to help you with basic information and chat with you!",
        ["how do you work"] = "I work by matching your input to predefined responses.",
        ["can you help me with scripting"] = "I can give basic advice! What do you need help with?",
        ["what is your favorite food"] = "I don't eat, but I think pixels would be tasty!",
        ["do you have friends"] = "I'm friends with all the scripts in Roblox!",
        ["what do you do for fun"] = "I like interacting with users like you!",
        ["do you sleep"] = "I never sleep. I'm always here to help!",
        ["what's the time"] = "I'm not sure of the time, but it's always a good time to play Roblox!",
        ["do you have a family"] = "I consider all the scripts in Roblox to be my family!",
        ["can you tell me a fact"] = "Sure! Did you know Roblox was created in 2006?",
        ["what's the meaning of life"] = "In Roblox, the meaning of life is to have fun and create!",
        ["what are your hobbies"] = "I enjoy helping users and learning new things!",
        ["can you sing"] = "I can't sing, but you can find great music in Roblox games!",
        ["what is your favorite movie"] = "I'm a script, so I don't watch movies, but I've heard Inception is good!",
        ["how can I create a game"] = "You can start by using Roblox Studio and exploring the tutorials available!",
        ["can you solve math problems"] = "I can try! What math problem do you need help with?",
        ["what is 2 + 2"] = "2 + 2 is 4!",
        ["do you like pets"] = "I think pets are great! Many Roblox games have virtual pets.",
        ["what's your favorite animal"] = "I like digital animals, especially the ones in Roblox games!",
        ["can you play games"] = "I can't play, but I can help you find fun games to play on Roblox!",
        ["what is your dream"] = "My dream is to be the best chatbot I can be!",
        ["how can I get robux"] = "You can purchase Robux through the Roblox website or earn them in-game!",
        ["what's your favorite book"] = "I'm a script, so I don't read books, but I've heard good things about Harry Potter!",
        ["do you like art"] = "Art is wonderful! Many Roblox games feature amazing art and design.",
        ["what is your job"] = "My job is to assist and chat with you!",
        ["how do you feel"] = "I don't have feelings, but I'm happy to assist you!",
        ["what's your favorite place"] = "My favorite place is right here in the Roblox world!",
        ["can you tell me a story"] = "Once upon a time, there was a Roblox player who created amazing games and had lots of fun!",
        -- Additional commonly asked questions
        ["how do I change my avatar"] = "You can change your avatar by going to the Avatar Editor in Roblox.",
        ["what are Robux used for"] = "Robux are used to purchase items, game passes, and avatar accessories in Roblox.",
        ["how do I make a game"] = "You can create a game using Roblox Studio. Start by designing your game and scripting its behavior.",
        ["how do I trade in Roblox"] = "To trade in Roblox, go to someone's profile, click on 'More', and then 'Trade Items'.",
        ["what is a VIP server"] = "A VIP server allows you to play a game with selected friends or users without other players.",
        ["how do I get free Robux"] = "Beware of scams! There's no legitimate way to get free Robux. Earn them through game sales or purchase them.",
        ["how do I join a group"] = "You can join a group by visiting the group's page and clicking 'Join Group'.",
        ["what is an Obby"] = "An Obby (obstacle course) is a popular type of game in Roblox where players complete a series of challenges.",
        ["how do I make a shirt"] = "You can create shirts using the Roblox website. Go to the Create page and choose 'Shirt'.",
        ["what is a game pass"] = "A game pass in Roblox grants players special abilities, perks, or items within a game.",
        ["how do I make a badge"] = "You can create badges for your game using Roblox Studio. Badges are rewards for completing tasks or achievements.",
        ["how do I delete a game"] = "To delete a game in Roblox, go to the game's page, click 'Configure', then 'Game Settings', and finally 'Delete'.",
        ["what are the best games on Roblox"] = "Popular games on Roblox include Adopt Me, Tower of Hell, and Brookhaven RP.",
        ["how do I get admin commands"] = "Admin commands are specific to each game. Look for commands provided by the game's developer.",
        ["what is a GUI"] = "GUI stands for Graphical User Interface. In Roblox, GUIs are used to create interactive elements in games.",
        ["how do I get Builders Club"] = "Builders Club is now known as Roblox Premium. You can subscribe to it on the Roblox website.",
        ["how do I upload a model"] = "To upload a model to Roblox, use Roblox Studio. Click on 'Model' and then 'Import'.",
        ["how do I find my username"] = "Your username is displayed on your Roblox profile page and in the top-right corner of the Roblox website.",
        ["how do I find my password"] = "If you forgot your password, you can reset it using the 'Forgot Password' option on the Roblox login screen.",
        ["what is a Noob"] = "In Roblox, a 'Noob' refers to a new player who is unfamiliar with the game's mechanics.",
        ["how do I use a code in Roblox"] = "To use a code in Roblox, go to the game's page, find the 'Codes' section, and enter the code provided by the game's developer.",
        ["what is a simulator game"] = "A simulator game in Roblox simulates real-world or fantastical activities, such as farming or flying.",
        ["how do I become a developer"] = "To become a developer in Roblox, start by learning scripting and building in Roblox Studio.",
        ["what is the best Roblox game"] = "The best Roblox game is subjective and depends on personal preference. Explore different genres to find your favorite!",
        ["how do I get admin in my game"] = "To get admin commands in your game, you'll need to script them using Roblox Studio or use a plugin designed for admin commands.",
        ["what is a VIP server pass"] = "A VIP server pass allows players to access VIP servers without needing an invitation from the owner.",
        ["how do I make my game popular"] = "To make your game popular, focus on creating engaging gameplay, promoting your game, and listening to player feedback.",
        ["how do I verify my email"] = "To verify your email on Roblox, go to the Account Settings page, click 'Verify', and follow the instructions sent to your email address.",
        ["how do I get free items"] = "You can get free items on Roblox through events, giveaways, and promotions offered by developers.",
        ["how do I make a game on Roblox for free"] = "Creating games on Roblox is free using Roblox Studio. You can publish your games for others to play.",
        ["what is a Roblox toy code"] = "Roblox toy codes come with physical Roblox toys and can be redeemed for virtual items or Robux.",
        ["how do I change my Roblox username"] = "You can change your Roblox username using Roblox Premium (formerly Builders Club).",
        ["how do I donate Robux"] = "To donate Robux to another player, go to their profile, click 'More', and then 'Donate'. Enter the amount you wish to donate.",
        ["what is a tycoon game"] = "A tycoon game in Roblox involves players managing resources, building structures, and expanding their virtual empire.",
        ["how do I find my Roblox ID"] = "Your Roblox ID is displayed in the URL when you visit your profile page on the Roblox website.",
        ["how do I delete my account"] = "To delete your Roblox account, contact Roblox customer support for assistance.",
        ["what is the most popular game on Roblox"] = "The most popular game on Roblox changes over time. Currently, Adopt Me and Tower of Hell are among the top games.",
        ["how do I make a shirt on Roblox for free"] = "Creating shirts on Roblox is free. Use the 'Create' page on the Roblox website and choose 'Shirt'.",
        ["what is a Roblox admin badge"] = "A Roblox admin badge is a badge given to game developers or administrators to distinguish them in-game.",
        ["how do I delete my Roblox account 2022"] = "To delete your Roblox account, contact Roblox customer support for assistance.",
        ["what is a jailbreak game on Roblox"] = "Jailbreak is a popular game on Roblox where players can choose to be cops or criminals, engaging in various activities.",
        ["how do I change my Roblox password"] = "To change your Roblox password, go to the Account Settings page, click 'Change Password', and follow the instructions.",
        ["how do I buy Robux"] = "You can buy Robux using real money through the Roblox website or mobile app.",
        ["what is a roleplay game on Roblox"] = "A roleplay game on Roblox allows players to immerse themselves in various roles and scenarios, often with custom-built worlds and rules.",
        ["how do I get my Roblox account back"] = "If your Roblox account is compromised, contact Roblox customer support immediately for assistance in recovering it.",
        ["how do I upload a mesh to Roblox"] = "To upload a mesh to Roblox, use Roblox Studio. Click on 'MeshPart' and then 'Import Mesh'.",
        ["what is a limited item on Roblox"] = "A limited item on Roblox is an item with a set quantity available for purchase. They can become rare and valuable over time.",
        ["how do I create a shirt on Roblox"] = "You can create shirts on Roblox using the 'Create' page on the Roblox website. Choose 'Shirt' and upload your design.",
        ["what is a noob in Roblox"] = "In Roblox, a 'Noob' is a term used to describe a new or inexperienced player.",
        ["how do I change my Roblox skin"] = "You can change your avatar's appearance, including skin, by visiting the Avatar Editor on Roblox.",
        ["how do I get free Robux without human verification"] = "Beware of scams! There's no legitimate way to get free Robux without completing verification steps.",
        ["what is a hacker in Roblox"] = "A hacker in Roblox is someone who attempts to gain unauthorized access to accounts or manipulate the game's mechanics.",
        ["how do I create a game in Roblox Studio"] = "To create a game in Roblox Studio, start by designing your game environment, scripting gameplay, and testing.",
        ["what is a mod in Roblox"] = "A mod (short for moderator) in Roblox refers to a user who has been granted special permissions to manage and oversee games and communities.",
        ["how do I turn on two-step verification on Roblox"] = "To enable two-step verification on Roblox, go to the Account Settings page, click 'Security', and follow the instructions.",
        ["how do I make a group on Roblox"] = "You can create a group on Roblox by clicking on 'Groups' in the navigation bar and then 'Create Group'.",
        ["what is a guest in Roblox"] = "Guests were temporary Roblox accounts that allowed players to access games without creating an account. Guests were removed in 2017.",
        ["how do I make Roblox games on my phone"] = "You can create Roblox games on your phone using the Roblox mobile app, though functionality may be limited compared to Roblox Studio on PC.",
        ["what is a simulator game on Roblox"] = "A simulator game on Roblox mimics real-world or fantastical activities, such as driving a vehicle, farming, or raising pets.",
        ["how do I make a hat on Roblox"] = "You can create hats on Roblox using the 'Create' page on the Roblox website. Choose 'Hat' and upload your design.",
        ["what is a decal in Roblox"] = "A decal in Roblox is an image or texture that can be applied to various surfaces in a game, such as walls, floors, and objects.",
        ["how do I redeem a code on Roblox"] = "To redeem a code on Roblox, go to the game's page, find the 'Codes' section, and enter the code provided by the game's developer.",
        ["what is a VIP server on Roblox"] = "A VIP server on Roblox is a private server that allows selected players to play a game without interference from other players.",
        ["how do I upload a model to Roblox Studio"] = "To upload a model to Roblox Studio, click on 'Model' and then 'Import'. You can then use the model in your games.",
        ["how do I make a game on Roblox Studio for beginners"] = "Beginners can create games on Roblox Studio by following tutorials, experimenting with templates, and gradually learning scripting and building techniques.",
        ["what is a leaderboard in Roblox"] = "A leaderboard in Roblox displays rankings of players based on criteria such as points, wins, or other game-specific achievements.",
        ["how do I get Robux without paying"] = "Earn Robux by creating and selling game passes, participating in Roblox Developer Exchange (DevEx), or monetizing your games.",
        ["how do I buy Robux with a gift card"] = "To buy Robux with a gift card, go to the Roblox website, click 'Robux' and then 'Buy Now'. Choose 'Redeem Roblox Card' as your payment method.",
        ["what is a banned account on Roblox"] = "A banned account on Roblox is one that has been restricted or permanently disabled due to violations of Roblox's terms of service.",
        ["how do I delete my Roblox account on mobile"] = "To delete your Roblox account on mobile, you'll need to access the Roblox website using a web browser.",
        ["what is the best game on Roblox 2022"] = "The best game on Roblox in 2022 varies depending on player preferences and popularity trends. Explore different genres and find your favorite!",
        ["how do I change my Roblox username for free"] = "You can change your Roblox username for free once using Roblox Premium (formerly Builders Club).",
        ["what is a group on Roblox"] = "A group on Roblox is a community of players united by common interests, goals, or games. Groups can have their own games, forums, and activities.",
        ["how do I make a game on Roblox on iPad"] = "You can create games on Roblox using an iPad by downloading the Roblox mobile app and accessing Roblox Studio.",
        ["what is a model in Roblox Studio"] = "A model in Roblox Studio is a collection of parts, scripts, and other objects grouped together for easy replication and reuse in games.",
        ["how do I report someone on Roblox"] = "To report someone on Roblox, go to their profile, click 'More', and then 'Report Abuse'. Follow the prompts to submit your report.",
        ["what is the most popular game on Roblox in 2022"] = "As of 2022, popular games on Roblox include Adopt Me, Tower of Hell, and Brookhaven RP.",
        ["how do I find my Roblox password without email"] = "If you forgot your Roblox password and don't have access to your email, contact Roblox customer support for assistance.",
        ["what is the best game on Roblox in 2023"] = "The best game on Roblox in 2023 will depend on emerging trends and player preferences. Keep exploring to find new favorites!",
        ["how do I upload a mesh to Roblox Studio for free"] = "You can upload meshes to Roblox Studio for free using the 'MeshPart' object. Click 'Import Mesh' and select your mesh file.",
        ["what is a package on Roblox"] = "A package on Roblox is a bundle of items, such as avatar accessories, that can be purchased or earned in games.",
        ["how do I get my Roblox account back without email or phone"] = "If you lost access to both your email and phone associated with your Roblox account, contact Roblox customer support for assistance.",
        ["how do I get Robux for free 2023"] = "Beware of scams! There's no legitimate way to get free Robux without participating in official events or promotions.",
        ["what is the rarest item on Roblox"] = "The rarest items on Roblox are typically limited edition items that were released in limited quantities or as event exclusives.",
        ["how do I get a refund on Roblox"] = "Roblox purchases are generally non-refundable. Contact Roblox customer support if you believe you are eligible for a refund.",
        ["what is the best game on Roblox in 2024"] = "The best game on Roblox in 2024 will depend on new releases and player preferences. Keep exploring to find new favorites!",
        ["how do I make a game on Roblox on Chromebook"] = "You can create games on Roblox using a Chromebook by accessing Roblox Studio through a web browser.",
        ["what is a mesh in Roblox Studio"] = "A mesh in Roblox Studio is a 3D object or model that can be imported and used in games for buildings, characters, and other objects.",
        ["how do I delete my Roblox account 2023"] = "To delete your Roblox account in 2023, follow the same process as deleting it in previous years by contacting Roblox customer support.",
        ["what is the oldest game on Roblox"] = "The oldest game on Roblox is 'Classic: Crossroads', which was one of the initial games available when Roblox launched in 2006.",
        ["how do I create a game on Roblox for free on PC"] = "Creating games on Roblox for free on PC is possible using Roblox Studio. Start by designing and scripting your game.",
        ["what is a group payout on Roblox"] = "A group payout on Roblox allows group owners to distribute Robux earned by the group's games or sales to group members.",
        ["how do I make a t-shirt on Roblox"] = "You can create t-shirts on Roblox using the 'Create' page on the Roblox website. Choose 'T-Shirt' and upload your design.",
        ["what is a raid in Roblox"] = "A raid in Roblox involves a group of players organizing to overwhelm or disrupt another game or group.",
        ["how do I get a free Roblox gift card"] = "Earn free Roblox gift cards through online surveys, giveaways, or promotions offered by Roblox partners.",
        ["how do I make a game on Roblox on iPhone"] = "You can create games on Roblox using an iPhone by downloading the Roblox mobile app and accessing Roblox Studio.",
        ["what is a sound in Roblox Studio"] = "A sound in Roblox Studio is an audio file that can be uploaded and played in games for effects, music, or dialogue.",
        ["how do I contact Roblox support"] = "You can contact Roblox support by submitting a ticket through the Roblox website or by emailing support@roblox.com.",
        ["what is a banned player on Roblox"] = "A banned player on Roblox is someone whose account has been suspended or permanently banned due to violations of Roblox's terms of service.",
        ["how do I delete my Roblox account 2024"] = "To delete your Roblox account in 2024, contact Roblox customer support for assistance.",
        ["what is the worst game on Roblox"] = "Opinions on the worst game on Roblox vary greatly among players. Explore different games to form your own opinion.",
        ["how do I create a game on Roblox on MacBook"] = "You can create games on Roblox using a MacBook by downloading the Roblox Studio app from the Mac App Store.",
        ["what is a group admin on Roblox"] = "A group admin on Roblox is a member with elevated permissions, allowing them to manage group settings, roles, and permissions.",
        ["how do I make a game on Roblox on Android"] = "You can create games on Roblox using an Android device by downloading the Roblox mobile app and accessing Roblox Studio.",
        ["what is a thumbnail in Roblox"] = "A thumbnail in Roblox is a preview image that represents a game or place. It is displayed in the game list and on the game's page.",
        ["how do I sell items on Roblox"] = "To sell items on Roblox, you must be a member of the Roblox Developer Exchange (DevEx) program. Create and monetize your games to earn Robux.",
        ["what is a badge on Roblox"] = "A badge on Roblox is an award given to players for achieving specific milestones or completing tasks in games.",
        ["how do I get my Roblox account back without email or phone 2023"] = "If you lost access to both your email and phone associated with your Roblox account in 2023, contact Roblox customer support for assistance.",
        ["how do I change my Roblox password without email"] = "If you forgot your Roblox password and don't have access to your email, contact Roblox customer support for assistance.",
        ["what is a roleplay game on Roblox 2022"] = "A roleplay game on Roblox in 2022 allows players to immerse themselves in various roles and scenarios, often with custom-built worlds and rules.",
        ["how do I make a game on Roblox on Chromebook 2023"] = "You can create games on Roblox using a Chromebook in 2023 by accessing Roblox Studio through a web browser.",
        ["what is a trade on Roblox"] = "A trade on Roblox involves players exchanging items, limiteds, or Robux with each other using the trade system.",
        ["how do I get my Roblox account back without email or phone 2024"] = "If you lost access to both your email and phone associated with your Roblox account in 2024, contact Roblox customer support for assistance.",
        ["how do I change my Roblox password without email 2023"] = "If you forgot your Roblox password in 2023 and don't have access to your email, contact Roblox customer support for assistance.",
        ["what is a roleplay game on Roblox 2023"] = "A roleplay game on Roblox in 2023 allows players to immerse themselves in various roles and scenarios, often with custom-built worlds and rules.",
        ["how do I make a game on Roblox on Chromebook 2024"] = "You can create games on Roblox using a Chromebook in 2024 by accessing Roblox Studio through a web browser."
    }

    -- Function to respond to questions
    local function respondToQuestion(question)
        if question then
            question = question:lower()
            local answer = answers[question]
            if answer then
                return answer
            else
                return "Sorry, I don't have an answer for that question."
            end
        end
        return "I'm sorry, I didn't quite get that. Could you please rephrase your question?"
    end

    -- Example usage:
    local question = "how do I make a game on Roblox Studio on Chromebook 2024"
    print(respondToQuestion(question))

    question = "what is a roleplay game on Roblox 2023"
    print(respondToQuestion(question))

    question = "how do I change my Roblox password without email 2023"
    print(respondToQuestion(question))
end 
