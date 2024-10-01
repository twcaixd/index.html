# index.html
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>戰鬥英雄</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #111;
            color: white;
            text-align: center;
        }
        #menu {
            margin-top: 50px;
        }
        button {
            padding: 15px 30px;
            margin: 10px;
            background-color: #FF5722;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #E64A19;
        }
        #characters {
            display: none;
            margin-top: 20px;
        }
        .character {
            margin: 10px;
            display: inline-block;
            background-color: #333;
            padding: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>戰鬥英雄</h1>
    <div id="menu">
        <button onclick="startGame()">開始遊戲</button>
        <button onclick="showCharacters()">選擇角色</button>
        <button onclick="settings()">設定</button>
        <button onclick="exitGame()">離開</button>
    </div>
    <div id="characters">
        <h2>選擇你的角色</h2>
        <div id="characterList"></div>
    </div>

    <script>
        const characters = [
            { name: "火焰戰士 - Blaze", skill: "火焰投擲" },
            { name: "冰霜獵手 - Frost", skill: "冰凍射擊" },
            { name: "狙擊專家 - Hawk", skill: "透視瞄準" },
            { name: "隱匿刺客 - Shadow", skill: "瞬間移動" },
            { name: "重裝炮手 - Titan", skill: "重型炮火" },
            { name: "電流使者 - Volt", skill: "電擊攻擊" },
            { name: "醫療兵 - Medic", skill: "急救包" },
            { name: "爆破專家 - Blast", skill: "炸藥設置" },
            { name: "鋼鐵護衛 - Ironclad", skill: "護盾" },
            { name: "風暴使者 - Storm", skill: "風暴召喚" },
            { name: "幽靈狙擊手 - Phantom", skill: "隱身" },
            { name: "毒素射手 - Venom", skill: "毒液箭" },
            { name: "機械大師 - Mech", skill: "機器人助手" },
            { name: "狙擊手 - Eagle", skill: "高空狙擊" },
            { name: "火箭兵 - Rocket", skill: "火箭發射" },
            { name: "電磁戰士 - Magnet", skill: "磁場干擾" },
            { name: "狂戰士 - Berserker", skill: "狂怒攻擊" },
            { name: "女戰士 - Valkyrie", skill: "空中突襲" },
            { name: "影子刺客 - Wraith", skill: "影子分身" },
            { name: "重型機槍手 - Gunner", skill: "掃射" },
            { name: "時空旅行者 - Chrono", skill: "時間暫停" },
            { name: "野獸獵人 - Hunter", skill: "野獸召喚" },
            { name: "火焰法師 - Ember", skill: "火焰旋風" },
            { name: "冰霜法師 - Glacius", skill: "冰霜屏障" },
            { name: "雷電法師 - Thunder", skill: "雷電鏈" },
            { name: "暗影法師 - Obsidian", skill: "黑暗魔法" },
            { name: "神秘法師 - Mystic", skill: "魔法護盾" },
            { name: "鋼鐵巨人 - Colossus", skill: "地面震撼" },
            { name: "光明使者 - Lumin", skill: "光明治療" },
            { name: "機器人戰士 - Robo", skill: "機器人攻擊" },
            { name: "幽靈獵手 - Specter", skill: "靈魂追擊" },
            { name: "戰鬥工程師 - Engineer", skill: "建造防禦" }
        ];

        function startGame() {
            alert("遊戲開始！");
            // 在這裡添加開始遊戲的邏輯
        }

        function showCharacters() {
            document.getElementById("menu").style.display = "none";
            document.getElementById("characters").style.display = "block";
            const characterList = document.getElementById("characterList");
            characterList.innerHTML = "";

            characters.forEach(character => {
                const div = document.createElement("div");
                div.className = "character";
                div.innerHTML = `<strong>${character.name}</strong><br>技能: ${character.skill}`;
                characterList.appendChild(div);
            });
        }

        function settings() {
            alert("這裡是設定選項！");
            // 在這裡添加設定的邏輯
        }

        function exitGame() {
            alert("遊戲結束，謝謝遊玩！");
            // 在這裡添加退出遊戲的邏輯
        }
    </script>
</body>
</html>
