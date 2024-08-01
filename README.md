<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Real Panjab</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        body {
            background-color: #f8f8f8;
            font-family: 'Times New Roman', serif;
        }
        .header {
            background-image: url('https://source.unsplash.com/random/1920x1080?sikh-warrior');
            background-size: cover;
            background-position: center;
            color: white;
        }
        .overlay {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
        }
    </style>
</head>
<body>
    <header class="header h-64 flex items-center justify-center">
        <div class="overlay text-center">
            <h1 class="text-4xl font-bold">The Real Panjab</h1>
            <p class="text-lg">Embracing the Heritage of Panjab</p>
        </div>
    </header>
    <main class="p-8">
        <section id="literature" class="mb-8">
            <h2 class="text-2xl font-bold mb-4">Literature Library</h2>
            <div id="literature-list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Literature Items -->
            </div>
        </section>
        <section id="music" class="mb-8">
            <h2 class="text-2xl font-bold mb-4">Punjabi Music</h2>
            <div id="music-list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Music Items -->
            </div>
        </section>
        <section id="videos" class="mb-8">
            <h2 class="text-2xl font-bold mb-4">Videos</h2>
            <div id="video-list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Video Items -->
            </div>
        </section>
        <section id="sikh-warriors" class="mb-8">
            <h2 class="text-2xl font-bold mb-4">Sikh Warriors</h2>
            <div id="warrior-list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Sikh Warrior Images -->
            </div>
        </section>
    </main>
    <footer class="text-center py-4">
        <p>&copy; 2024 The Real Panjab. All rights reserved.</p>
    </footer>
</body>
<script>
    const literatureList = [
        {title: 'Poetry 1', description: 'Description of Poetry 1'},
        {title: 'Poetry 2', description: 'Description of Poetry 2'},
        // Add more items
    ];
    const musicList = [
        {title: 'Song 1', url: 'https://example.com/song1.mp3'},
        {title: 'Song 2', url: 'https://example.com/song2.mp3'},
        // Add more items
    ];
    const videoList = [
        {title: 'Video 1', url: 'https://example.com/video1.mp4'},
        {title: 'Video 2', url: 'https://example.com/video2.mp4'},
        // Add more items
    ];
    const warriorList = [
        {image: 'https://source.unsplash.com/random/1920x1080?sikh-warrior-1'},
        {image: 'https://source.unsplash.com/random/1920x1080?sikh-warrior-2'},
        // Add more items
    ];

    function populateList(listId, items, isImage = false) {
        const list = document.getElementById(listId);
        items.forEach(item => {
            const div = document.createElement('div');
            div.className = 'p-4 bg-white shadow rounded';
            if (isImage) {
                const img = document.createElement('img');
                img.src = item.image;
                img.alt = item.title || '';
                img.className = 'w-full h-48 object-cover rounded';
                div.appendChild(img);
            } else {
                const h3 = document.createElement('h3');
                h3.className = 'text-xl font-bold mb-2';
                h3.textContent = item.title;
                div.appendChild(h3);
                const p = document.createElement('p');
                p.textContent = item.description || item.url;
                div.appendChild(p);
            }
            list.appendChild(div);
        });
    }

    document.addEventListener('DOMContentLoaded', () => {
        populateList('literature-list', literatureList);
        populateList('music-list', musicList);
        populateList('video-list', videoList);
        populateList('warrior-list', warriorList, true);
    });
</script>

