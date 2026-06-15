+++
date = '2026-06-14T13:59:38-04:00'
draft = false
title = 'The White House Ufc and Gravlax. Pasta, Petunias, Hot Water in the Garden.'
author = 'Adeptus'
tags = ["Combat Sports", "dementia"]
authorImage = 'adeptus.jpg'
+++

## What are we doing here?

Today is a little weird. Things feel off. I hope this doesn't mean something bad is going to happen at the White House UFC. I do love combat sports and this UFC event is a little wild. I mean, putting it at the WH is crazy on its face, but then banning Strickland and all the weird hubbub going into it with Hokit. I dunno. Things feel especially off because my mom was threatening to kill herself yesterday, but when cops showed up to check on her she was just complaining about not being able to pay movers because shes broke. She keeps giving all her money away to Elon Musk scammers. She thinks they're engaged and he needs gift cards. She's going crazy. I can't do much to get her to listen to me. I really hope she does not end up trying to leave her apartment at the end of this month because she will have nowhere to go. It's pretty bad.

> [!Caution]
> Some parents will go crazy when then get old. It will suck.

Back to the UFC. It's weird that there is no undercard, but all the fights are bangers. It's going to be great as long as nobody tries to do anything bad, because honestly, its an easy target event-wise for something bad to happen. The weather is going to be bad and people on bluesky are talking about it. I don't have a bluesky account but my Aunt does and she regularly sends me links from it. I prefer the good old fashioned Twitter/X and its funny because I never really used or paid attention to it until it became X.

I feel like im just wandering. Floating. Aimless. I want to be able to help my mom. I want her to be able to not be so frustrated and upset about things. I wish she would listen to me. There are only 2 people trying to help and look out for her and she thinks we're obstacles in the way of her happiness.

I dont have much to say today. I havent been eating or sleeping or exercising well. I dont feel great. I'm programming a bit. Fights are on. I hope its good. Distract me please.

<canvas style="border: 2px solid #333; display: block; margin: 20px auto; background-color: #f0f0f0;" id="gameCanvas" width="600" height="400"></canvas>

<script>
    // 1. Setup Canvas
    const canvas = document.getElementById('gameCanvas');
    const ctx = canvas.getContext('2d');

    // 2. Game State
    const player = {
        x: 50,
        y: 50,
        width: 30,
        height: 30,
        speed: 5,
        color: '#3498db'
    };

    const keys = {};

    // 3. Input Handling
    document.addEventListener('keydown', (e) => {
        keys[e.key] = true;
    });

    document.addEventListener('keyup', (e) => {
        keys[e.key] = false;
    });

    // 4. Game Logic (Update)
    function update() {
        if (keys['ArrowUp'] && player.y > 0) player.y -= player.speed;
        if (keys['ArrowDown'] && player.y < canvas.height - player.height) player.y += player.speed;
        if (keys['ArrowLeft'] && player.x > 0) player.x -= player.speed;
        if (keys['ArrowRight'] && player.x < canvas.width - player.width) player.x += player.speed;
    }

    // 5. Rendering (Draw)
    function draw() {
        // Clear screen
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Draw player
        ctx.fillStyle = player.color;
        ctx.fillRect(player.x, player.y, player.width, player.height);
    }

    // 6. Game Loop
    function gameLoop() {
        update();
        draw();
        requestAnimationFrame(gameLoop);
    }

    // Start the game
    gameLoop();
</script>
