<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tap Repair Game</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Import the Inter font for a clean, modern look */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');

        /* Global styles for the body */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #1f2937; /* Darker background */
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
            touch-action: manipulation;
            color: #d1d5db;
        }

        /* Main container for the game */
        .container {
            max-width: 600px;
            background-color: #374151; /* Lighter background for the card */
        }

        /* Game canvas styling and animations */
        .game-canvas {
            cursor: pointer;
            width: 100%;
            min-height: 300px;
            background-color: #4b5563;
            transition: transform 0.1s ease-out, box-shadow 0.2s ease-in-out;
            will-change: transform, box-shadow;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 1rem;
            box-shadow: 0 10px 15px rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden;
        }
        .game-canvas:active {
            transform: scale(0.98);
            box-shadow: 0 5px 10px rgba(0,0,0,0.2);
        }

        /* Message box for success/fail popups */
        .message-box {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            padding: 1rem 2rem;
            border-radius: 0.75rem;
            z-index: 100;
            animation: fadeOut 1.5s forwards;
            font-size: 1.25rem;
            font-weight: 700;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        .message-success {
            background-color: #34d399; /* Green */
            color: white;
        }
        .message-fail {
            background-color: #f87171; /* Red */
            color: white;
        }
        @keyframes fadeOut {
            0% { opacity: 1; transform: translate(-50%, -50%) scale(1); }
            50% { opacity: 1; }
            100% { opacity: 0; transform: translate(-50%, -50%) scale(0.9); }
        }
        
        /* Button styling with animations */
        .btn-game {
            transition: transform 0.1s ease-out, box-shadow 0.2s ease-in-out;
            font-weight: 700;
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 0.75rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .btn-game:active {
            transform: scale(0.95);
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .btn-green { background: linear-gradient(145deg, #10b981, #059669); }
        .btn-blue { background: linear-gradient(145deg, #3b82f6, #2563eb); }
        .btn-purple { background: linear-gradient(145deg, #a855f7, #9333ea); }
        .btn-upgrade { background: #4b5563; color: #d1d5db; transition: all 0.2s ease-in-out; }
        .btn-upgrade:not([disabled]):hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 10px rgba(0,0,0,0.2);
            background: linear-gradient(145deg, #10b981, #059669);
            color: white;
        }
        .btn-upgrade[disabled] { cursor: not-allowed; opacity: 0.5; }

        /* Tech emoji animation */
        #tech-emoji-display {
            font-size: 8rem;
            line-height: 1;
            transition: transform 0.3s ease-out;
            animation: pulse 2s infinite ease-in-out;
        }
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Repair bar styling */
        .repair-bar-container {
            width: 80%;
            height: 24px;
            background-color: #6b7280;
            border-radius: 9999px;
            overflow: hidden;
            margin-top: 1.5rem;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.2);
        }
        .repair-bar {
            height: 100%;
            background: linear-gradient(90deg, #60a5fa, #3b82f6);
            transition: width 0.1s ease-out;
        }

        /* Customer container with message bubble */
        #customer-container {
            display: flex;
            align-items: flex-end;
            justify-content: flex-end; /* Align to the right side */
            gap: 1rem;
            min-height: 4rem;
        }
        #customer-message-bubble {
            background-color: #e5e7eb;
            color: #1f2937;
            padding: 0.5rem 1rem;
            border-radius: 1rem 1rem 1rem 0; /* Chat bubble shape */
            position: relative;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
            font-size: 0.875rem;
            max-width: 70%;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        #customer-message-bubble::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: -10px; /* Point to the right */
            width: 0;
            height: 0;
            border-style: solid;
            border-width: 0 0 10px 10px;
            border-color: transparent transparent #e5e7eb transparent;
        }
        #customer-svg {
            animation: bobbing 2s infinite ease-in-out;
            height: 50px;
            width: 50px;
            transition: transform 0.2s ease-in-out;
        }
        .mouth, .eyebrows {
            display: none;
        }
        .show-face {
            display: block;
        }
        .shake {
            animation: shake 0.5s ease-in-out;
        }
        @keyframes bobbing {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            50% { transform: translateX(5px); }
            75% { transform: translateX(-5px); }
        }
    </style>
    <!-- Tone.js for sound effects -->
    <script src="https://cdn.jsdelivr.net/npm/tone@14.7.58/build/Tone.min.js"></script>
</head>
<body class="flex items-center justify-center min-h-screen p-4">
    <div id="game-container" class="container w-full rounded-xl shadow-2xl p-6">
        <!-- Start Menu with Story -->
        <div id="start-menu" class="flex flex-col items-center gap-6 text-center animate-fadeIn">
            <h1 class="text-4xl font-black text-white">TAP REPAIR GAME</h1>
            <div id="story-text" class="bg-gray-800 p-6 rounded-lg shadow-inner text-gray-300 text-base md:text-lg text-left">
                <!-- Story text will be displayed here -->
            </div>
            <button id="start-game-button" class="btn-game btn-green w-full">
                Start Game
            </button>
        </div>

        <!-- Main Game UI (Hidden by default) -->
        <div id="main-game-ui" class="hidden flex flex-col items-center gap-4">
            <div class="w-full flex justify-between text-lg font-bold text-gray-300">
                <span>Day: <span id="day-number">1</span></span>
                <span>Time Left: <span id="day-timer">2:00</span></span>
            </div>
            <div class="w-full text-center text-2xl font-black text-white">
                <span id="coin-display">0</span> Coins
            </div>

            <!-- Tap area for repairs -->
            <div id="game-canvas" class="game-canvas rounded-lg shadow-lg">
                <p id="tech-emoji-display" class="w-2/3 h-2/3 flex items-center justify-center p-4">
                    <!-- Emoji will be injected here -->
                </p>
                <p id="tech-name-display" class="text-xl font-bold text-gray-300 mt-2">Tech Name</p>
                <div class="repair-bar-container">
                    <div id="repair-bar" class="repair-bar" style="width: 0%;"></div>
                </div>
                <p id="repair-speed-display" class="text-sm text-gray-400 mt-4">Tap Speed: 0/s</p>
            </div>

            <!-- Customer and Message Bubble -->
            <div id="customer-container" class="w-full flex justify-end items-end p-2">
                <div id="customer-message-bubble" class="hidden"></div>
                <svg id="customer-svg" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
                    <!-- Body and Head -->
                    <path fill-rule="evenodd" d="M7.5 6a4.5 4.5 0 119 0 4.5 4.5 0 01-9 0zM3.751 20.105a8.25 8.25 0 0116.498 0 .75.75 0 01-.255.518l-.066.059.135.25a6.643 6.643 0 01-1.396 1.48c-.966.602-2.09.98-3.323 1.157L12 23.25l-.255-.038c-1.233-.177-2.357-.555-3.323-1.157a6.643 6.643 0 01-1.396-1.48l.135-.25-.066-.059a.75.75 0 01-.255-.518z" clip-rule="evenodd" />
                    <!-- Eyes -->
                    <circle cx="9.5" cy="7" r="0.75" fill="#ffffff"/>
                    <circle cx="14.5" cy="7" r="0.75" fill="#ffffff"/>
                    <!-- Neutral Face -->
                    <path id="mouth-neutral" class="mouth show-face" d="M9 10h6" stroke="#ffffff" stroke-width="0.75" stroke-linecap="round" fill="none"/>
                    <!-- Laughing Face -->
                    <path id="mouth-laugh" class="mouth" d="M10 10.5c1.5 1.5 4 1.5 5.5 0" stroke="#ffffff" stroke-width="0.75" stroke-linecap="round" fill="none"/>
                    <!-- Angry Face -->
                    <path id="mouth-angry" class="mouth" d="M10 11c1.5-1.5 4-1.5 5.5 0" stroke="#ffffff" stroke-width="0.75" stroke-linecap="round" fill="none"/>
                    <path id="eyebrow-angry-left" class="eyebrows" d="M8.5 5.5L10 6.5" stroke="#ffffff" stroke-width="0.75" stroke-linecap="round" fill="none"/>
                    <path id="eyebrow-angry-right" class="eyebrows" d="M15.5 5.5L14 6.5" stroke="#ffffff" stroke-width="0.75" stroke-linecap="round" fill="none"/>
                </svg>
            </div>
            
            <div id="message-container" class="relative w-full h-10"></div>
        </div>

        <!-- End of Day Summary and Shop -->
        <div id="end-of-day-ui" class="hidden flex flex-col items-center gap-4 text-center">
            <h2 class="text-2xl font-black text-white">Day <span id="summary-day-number"></span> Complete!</h2>
            <div class="w-full flex flex-col gap-2 p-4 bg-gray-800 rounded-lg shadow-md text-gray-300">
                <p class="text-lg">Coins Gained: <span id="summary-coins-gained" class="font-black text-green-400"></span></p>
                <p class="text-lg">Coins Lost: <span id="summary-coins-lost" class="font-black text-red-400"></span></p>
                <p class="text-lg">Successful Repairs: <span id="summary-repairs-successful" class="font-black"></span></p>
                <p class="text-lg">Failed Repairs: <span id="summary-repairs-failed" class="font-black"></span></p>
            </div>
            
            <h3 class="text-xl font-bold mt-4 text-gray-300">Shop</h3>
            <div class="w-full grid grid-cols-1 md:grid-cols-2 gap-4" id="upgrade-container">
                <!-- Shop buttons will be injected here by JS -->
            </div>
            
            <button id="next-day-button" class="btn-game btn-blue w-full mt-4">
                Start Next Day
            </button>
        </div>
        
        <!-- Sounds Button -->
        <button id="sounds-button" class="btn-game btn-purple w-full mt-4">
            Enable Sounds
        </button>
    </div>

    <script>
        // Game State Variables
        let coins = 0;
        let dayNumber = 1;
        const dayDuration = 2 * 60 * 1000; // Day duration is now 2 minutes
        let dayStartTime = 0;
        let gameInterval;
        let gameActive = false;

        // Repair Stats
        let repairsSuccessful = 0;
        let repairsFailed = 0;
        let coinsGainedThisDay = 0;
        let coinsLostThisDay = 0;
        
        // Repair Bar variables
        let repairProgress = 0;
        let tapsNeeded = 10;
        let tapsNeededReduction = 0; 

        // Tapping Logic
        let lastTapTime = 0;
        const tapTimes = [];
        let tapSpeed = 0;

        // Game Mechanics
        let baseFailChance = 0.05;
        let failChanceMultiplier = 0.01;
        let coinGainPerRepair = 10;
        let coinLossPerFailure = 5;

        // Upgrade System
        const upgrades = {
            'fail-reduction': {
                name: 'Reduce Fail Chance',
                description: 'Reduces the base chance of failure.',
                cost: 100,
                costIncrease: 100,
                level: 0,
                apply: () => { baseFailChance = Math.max(0, baseFailChance - 0.02); }
            },
            'coin-boost': {
                name: 'Increase Coin Gain',
                description: 'Increases the coins gained per successful repair.',
                cost: 150,
                costIncrease: 150,
                level: 0,
                apply: () => { coinGainPerRepair += 5; }
            },
            'fail-penalty': {
                name: 'Reduce Fail Penalty',
                description: 'Reduces the coins lost on a failed repair.',
                cost: 120,
                costIncrease: 120,
                level: 0,
                apply: () => { coinLossPerFailure = Math.max(0, coinLossPerFailure - 2); }
            },
            'tap-reduction': {
                name: 'Speedy Fingers',
                description: 'Reduces the number of taps needed for a repair.',
                cost: 200,
                costIncrease: 200,
                level: 0,
                apply: () => { tapsNeededReduction++; }
            }
        };

        // Tech Emoji Logic
        const techItems = [
            { name: "Smartphone", emoji: "📱" },
            { name: "Laptop", emoji: "💻" },
            { name: "Smartwatch", emoji: "⌚" },
            { name: "Tablet", emoji: "📱" },
            { name: "Headphones", emoji: "🎧" },
            { name: "Smart Speaker", emoji: "🔊" },
            { name: "VR Headset", emoji: "🥽" },
            { name: "Game Controller", emoji: "🎮" },
            { name: "Projector", emoji: "📽️" },
            { name: "Drone", emoji: "🚁" },
            { name: "Security Camera", emoji: "📹" },
            { name: "Robot Vacuum", emoji: "🤖" },
            { name: "Graphics Card", emoji: "🖲️" },
            { name: "Mouse", emoji: "🖱️" },
            { name: "Webcam", emoji: "📷" },
            { name: "Keyboard", emoji: "⌨️" },
            { name: "Power Bank", emoji: "🔋" },
            { name: "Bluetooth Speaker", emoji: "📻" },
            { name: "Monitor", emoji: "🖥️" },
            { name: "Router", emoji: "📡" }
        ];
        let currentTechItem = {};

        // Customer Success Messages
        const customerSuccessMessages = [
            "Thank you so much! It's working like new!",
            "You're a lifesaver!",
            "I can't believe you fixed it so quickly!",
            "My day is saved!",
            "Amazing work! I'll be back for sure.",
            "Wow! I thought this was completely broken.",
            "You're a true master of tech!"
        ];
        
        // Customer Failure Messages
        const customerFailureMessages = [
            "Oh no! What happened?!",
            "Are you sure you know what you're doing?",
            "Please be more careful...",
            "This isn't good. My device was just broken, now it's more broken!",
            "I can't afford to lose more coins...",
            "This is unacceptable!",
            "Maybe I should have gone somewhere else."
        ];
        
        // DOM Elements
        const startMenu = document.getElementById('start-menu');
        const mainGameUI = document.getElementById('main-game-ui');
        const startGameButton = document.getElementById('start-game-button');
        const storyText = document.getElementById('story-text');

        const coinDisplay = document.getElementById('coin-display');
        const dayNumberDisplay = document.getElementById('day-number');
        const dayTimerDisplay = document.getElementById('day-timer');
        const gameCanvas = document.getElementById('game-canvas');
        const endOfDayUI = document.getElementById('end-of-day-ui');
        const summaryDayNumber = document.getElementById('summary-day-number');
        const summaryCoinsGained = document.getElementById('summary-coins-gained');
        const summaryCoinsLost = document.getElementById('summary-coins-lost');
        const summaryRepairsSuccessful = document.getElementById('summary-repairs-successful');
        const summaryRepairsFailed = document.getElementById('summary-repairs-failed');
        const upgradeContainer = document.getElementById('upgrade-container');
        const nextDayButton = document.getElementById('next-day-button');
        const repairSpeedDisplay = document.getElementById('repair-speed-display');
        const messageContainer = document.getElementById('message-container');
        const customerMessageBubble = document.getElementById('customer-message-bubble');
        const techEmojiDisplay = document.getElementById('tech-emoji-display');
        const techNameDisplay = document.getElementById('tech-name-display');
        const repairBar = document.getElementById('repair-bar');
        const soundsButton = document.getElementById('sounds-button');
        const customerSvg = document.getElementById('customer-svg');

        const mouthNeutral = document.getElementById('mouth-neutral');
        const mouthLaugh = document.getElementById('mouth-laugh');
        const mouthAngry = document.getElementById('mouth-angry');
        const eyebrowAngryLeft = document.getElementById('eyebrow-angry-left');
        const eyebrowAngryRight = document.getElementById('eyebrow-angry-right');


        // Story Text
        const story = `
            Our story begins with a man named Jack. Tired of the corporate world, he decided to follow his passion: fixing things. He opened a small repair shop, a beacon of hope for all the broken gadgets and forgotten devices in the city. But the world of a one-man-shop is challenging, with endless repairs and limited time. Your mission is to help Jack grow his business, repair as many items as you can, and become a master technician!
        `;

        // Sound Logic
        let isSoundEnabled = false;
        let successSynth, failSynth, clickSynth;
        
        // Function to set up the Tone.js synths
        function setupSounds() {
            // A simple synth for a successful "ding" sound
            successSynth = new Tone.Synth({
                oscillator: { type: "sine" },
                envelope: {
                    attack: 0.005,
                    decay: 0.1,
                    sustain: 0.1,
                    release: 0.2
                }
            }).toDestination();
            successSynth.volume.value = -12;

            // A noise synth for a failed "buzz" or "thud" sound
            failSynth = new Tone.NoiseSynth({
                noise: { type: "brown" },
                envelope: {
                    attack: 0.001,
                    decay: 0.3,
                    sustain: 0,
                }
            }).toDestination();
            failSynth.volume.value = -10;

            // A membrane synth for a click sound
            clickSynth = new Tone.MembraneSynth({
                pitchDecay: 0.008,
                octaves: 1,
                oscillator: { type: 'sine' },
                envelope: {
                    attack: 0.001,
                    decay: 0.4,
                    sustain: 0.01,
                    release: 0.1
                }
            }).toDestination();
            clickSynth.volume.value = -15;
        }

        // Functions to play the sounds
        function playSuccessSound() {
            if (isSoundEnabled) {
                successSynth.triggerAttackRelease("G4", "8n");
            }
        }
        
        function playFailSound() {
            if (isSoundEnabled) {
                failSynth.triggerAttackRelease("4n");
            }
        }

        function playClickSound() {
            if (isSoundEnabled) {
                clickSynth.triggerAttackRelease("C3", "32n");
            }
        }
        
        // Function to enable/disable sounds
        function toggleSounds() {
            if (isSoundEnabled) {
                isSoundEnabled = false;
                soundsButton.textContent = "Enable Sounds";
            } else {
                // Browsers require a user gesture to start the audio context
                Tone.start().then(() => {
                    if (!successSynth) {
                        setupSounds();
                    }
                    isSoundEnabled = true;
                    soundsButton.textContent = "Disable Sounds";
                });
            }
        }

        // Function to update the customer's face
        function updateCustomerFace(mood) {
            // Hide all face parts
            mouthNeutral.classList.remove('show-face');
            mouthLaugh.classList.remove('show-face');
            mouthAngry.classList.remove('show-face');
            eyebrowAngryLeft.classList.remove('show-face');
            eyebrowAngryRight.classList.remove('show-face');
            
            // Show the correct face parts based on mood
            if (mood === 'neutral') {
                mouthNeutral.classList.add('show-face');
                customerSvg.classList.remove('shake');
            } else if (mood === 'laugh') {
                mouthLaugh.classList.add('show-face');
                customerSvg.classList.remove('shake');
            } else if (mood === 'angry') {
                mouthAngry.classList.add('show-face');
                eyebrowAngryLeft.classList.add('show-face');
                eyebrowAngryRight.classList.add('show-face');
                customerSvg.classList.add('shake');
            }
        }

        // Function to create and show a temporary message
        function showMessage(text, type) {
            const messageBox = document.createElement('div');
            messageBox.textContent = text;
            messageBox.className = `message-box ${type}`;
            messageContainer.appendChild(messageBox);

            // Remove the message box after its animation ends
            setTimeout(() => {
                messageBox.remove();
            }, 1500);
        }

        // Function to display a random customer success message
        function displayCustomerSuccessMessage() {
            const randomMessage = customerSuccessMessages[Math.floor(Math.random() * customerSuccessMessages.length)];
            customerMessageBubble.textContent = randomMessage;
            customerMessageBubble.classList.remove('hidden');
            customerMessageBubble.style.opacity = '1';
            
            setTimeout(() => {
                customerMessageBubble.style.opacity = '0';
                setTimeout(() => customerMessageBubble.classList.add('hidden'), 500); // Hide the bubble after it fades out
            }, 2500);
        }

        // Function to display a random customer failure message
        function displayCustomerFailureMessage() {
            const randomMessage = customerFailureMessages[Math.floor(Math.random() * customerFailureMessages.length)];
            customerMessageBubble.textContent = randomMessage;
            customerMessageBubble.classList.remove('hidden');
            customerMessageBubble.style.opacity = '1';
            
            setTimeout(() => {
                customerMessageBubble.style.opacity = '0';
                setTimeout(() => customerMessageBubble.classList.add('hidden'), 500); // Hide the bubble after it fades out
            }, 2500);
        }


        // Function to handle a repair attempt
        function attemptRepair() {
            if (!gameActive) return;
            playClickSound(); // Play the click sound on every tap

            // Update tap speed based on recent taps
            const currentTime = Date.now();
            if (lastTapTime > 0) {
                tapTimes.push(currentTime - lastTapTime);
            }
            lastTapTime = currentTime;

            // Keep track of the last few tap times for a more responsive average
            if (tapTimes.length > 5) {
                tapTimes.shift();
            }

            // Calculate average tap speed in taps per second
            if (tapTimes.length > 0) {
                const totalTime = tapTimes.reduce((a, b) => a + b, 0);
                const averageTime = totalTime / tapTimes.length;
                tapSpeed = Math.round(1000 / averageTime);
            } else {
                tapSpeed = 0;
            }
            
            // Display tap speed
            repairSpeedDisplay.textContent = `Tap Speed: ${tapSpeed}/s`;

            // Calculate actual fail chance based on tap speed
            const currentFailChance = baseFailChance + (tapSpeed * failChanceMultiplier);

            // Check if the repair fails on this tap
            if (Math.random() < currentFailChance) {
                playFailSound();
                // If it fails, reset progress
                repairProgress = 0;
                coins -= coinLossPerFailure;
                coinsLostThisDay += coinLossPerFailure;
                repairsFailed++;
                showMessage(`Failed! Lost ${coinLossPerFailure} Coins.`, 'message-fail');
                updateCustomerFace('angry');
                displayCustomerFailureMessage();
            } else {
                updateCustomerFace('neutral'); // Revert to neutral on a successful tap
                // If it doesn't fail, increase progress
                repairProgress++;
                // Check if the item is fully repaired
                if (repairProgress >= tapsNeeded) {
                    playSuccessSound();
                    coins += coinGainPerRepair;
                    coinsGainedThisDay += coinGainPerRepair;
                    repairsSuccessful++;
                    showMessage(`Success! Gained ${coinGainPerRepair} Coins.`, 'message-success');
                    displayCustomerSuccessMessage(); // Show customer message on successful repair
                    updateCustomerFace('laugh');
                    setTimeout(() => updateCustomerFace('neutral'), 3000); // Revert to neutral after a short delay
                    // Reset progress and get a new item
                    repairProgress = 0;
                    changeTechItem();
                }
            }
            updateUI();
        }
        
        // Function to change the emoji and name of the tech being repaired
        function changeTechItem() {
            let newItem;
            do {
                newItem = techItems[Math.floor(Math.random() * techItems.length)];
            } while (newItem.name === currentTechItem.name); // Ensure the new item is not the same as the previous one
            
            currentTechItem = newItem;
            techEmojiDisplay.textContent = currentTechItem.emoji;
            techNameDisplay.textContent = currentTechItem.name;

            // Set a new random number of taps needed for the new item, adjusted by upgrades
            const minTaps = 5;
            const maxTaps = 15;
            const effectiveMaxTaps = Math.max(minTaps, maxTaps - tapsNeededReduction);
            tapsNeeded = Math.floor(Math.random() * (effectiveMaxTaps - minTaps + 1)) + minTaps;
        }

        // Function to update the main game UI
        function updateUI() {
            coinDisplay.textContent = coins;
            dayNumberDisplay.textContent = dayNumber;

            const timePassed = Date.now() - dayStartTime;
            const timeLeft = Math.max(0, dayDuration - timePassed);
            const minutes = Math.floor(timeLeft / 60000);
            const seconds = Math.floor((timeLeft % 60000) / 1000);
            dayTimerDisplay.textContent = `${minutes}:${seconds < 10 ? '0' : ''}${seconds}`;

            // Update repair bar
            const progressPercentage = (repairProgress / tapsNeeded) * 100;
            repairBar.style.width = `${progressPercentage}%`;

            if (timeLeft <= 0 && gameActive) {
                endDay();
            }
        }

        // Function to start the game
        function startGame() {
            startMenu.classList.add('hidden');
            mainGameUI.classList.remove('hidden');
            startNewDay();
        }

        // Function to start a new day
        function startNewDay() {
            // Reset daily stats
            repairsSuccessful = 0;
            repairsFailed = 0;
            coinsGainedThisDay = 0;
            coinsLostThisDay = 0;
            tapTimes.length = 0;
            tapSpeed = 0;
            repairProgress = 0; // Reset progress bar at the start of a new day
            changeTechItem(); // Get a new item
            updateCustomerFace('neutral'); // Reset customer face to neutral at the start of a new day

            mainGameUI.classList.remove('hidden');
            endOfDayUI.classList.add('hidden');
            dayStartTime = Date.now();
            gameActive = true;
            gameInterval = setInterval(updateUI, 1000);
            updateUI();
        }

        // Function to end the current day and show the summary
        function endDay() {
            gameActive = false;
            clearInterval(gameInterval);
            dayNumber++;
            
            // Populate summary screen
            summaryDayNumber.textContent = dayNumber - 1;
            summaryCoinsGained.textContent = coinsGainedThisDay;
            summaryCoinsLost.textContent = coinsLostThisDay;
            summaryRepairsSuccessful.textContent = repairsSuccessful;
            summaryRepairsFailed.textContent = repairsFailed;
            
            // Populate upgrades
            renderUpgrades();

            mainGameUI.classList.add('hidden');
            endOfDayUI.classList.remove('hidden');
        }

        // Function to render upgrade buttons
        function renderUpgrades() {
            upgradeContainer.innerHTML = '';
            for (const key in upgrades) {
                const upgrade = upgrades[key];
                const button = document.createElement('button');
                button.className = `btn-upgrade p-4 rounded-lg shadow-md transition-all duration-200 text-left ${coins >= upgrade.cost ? '' : 'bg-gray-200 text-gray-500 cursor-not-allowed'}`;
                button.disabled = coins < upgrade.cost;
                button.innerHTML = `
                    <p class="font-bold text-lg">${upgrade.name}</p>
                    <p class="text-sm">${upgrade.description}</p>
                    <p class="text-sm mt-2">Cost: ${upgrade.cost} Coins (Level ${upgrade.level + 1})</p>
                `;
                button.addEventListener('click', () => {
                    if (coins >= upgrade.cost) {
                        coins -= upgrade.cost;
                        upgrade.level++;
                        upgrade.cost += upgrade.costIncrease;
                        upgrade.apply();
                        renderUpgrades();
                        updateUI();
                    }
                });
                upgradeContainer.appendChild(button);
            }
        }

        // Event listeners
        gameCanvas.addEventListener('mousedown', (e) => {
            if (gameActive) {
                attemptRepair();
            }
        });
        gameCanvas.addEventListener('touchstart', (e) => {
            if (gameActive) {
                e.preventDefault();
                attemptRepair();
            }
        });

        nextDayButton.addEventListener('click', () => {
            startNewDay();
        });

        soundsButton.addEventListener('click', () => {
            toggleSounds();
        });

        startGameButton.addEventListener('click', () => {
            startGame();
        });

        // Initialize the game when the window loads
        window.onload = function() {
            storyText.textContent = story.trim();
        }
    </script>
</body>
</html>
