<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>0xT3sla | WhoAmI</title>
    <style>
        :root {
            --bg-color: #0a0a0a;
            --main-color: #00ff41; /* أخضر التيرمينال */
            --text-color: #e0e0e0;
            --accent-color: #333;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: 'Courier New', Courier, monospace;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .terminal-window {
            background: #111;
            border: 1px solid var(--accent-color);
            border-radius: 8px;
            width: 100%;
            max-width: 700px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.8);
            overflow: hidden;
        }

        .terminal-header {
            background: #222;
            padding: 10px;
            display: flex;
            gap: 8px;
            border-bottom: 1px solid var(--accent-color);
        }

        .dot { width: 12px; height: 12px; border-radius: 50%; }
        .red { background: #ff5f56; }
        .yellow { background: #ffbd2e; }
        .green { background: #27c93f; }

        .content { padding: 40px; line-height: 1.8; }

        h1 { color: var(--main-color); font-size: 2rem; margin-bottom: 5px; letter-spacing: 2px; }
        
        .command { color: #888; margin-bottom:
