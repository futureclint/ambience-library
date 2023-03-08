<template>
  <div class="videos-list">
    <h1>Ambience Library</h1>
    <div class="list-wrap">
      <div v-for="video in videos" :key="video.id" :id="video.id" class="video">
        <h3>{{ video.title }}</h3>
        <div class="video-wrap">
            <iframe width="480" height="270" :src="video.href" :title="video.title" frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="tag-wrap">
          <div>Tags</div>
          <span v-for="tag in video.tags">{{ tag }}</span>
        </div>
    </div>
    </div>
  </div>
</template>
<style>
  .videos-list {
    display: flex;
    flex-direction: column;
  }
  .videos-list .list-wrap {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: start;
    align-items: auto;
    align-content: start;

  }
  @media screen and (max-width: 500px) {
    .videos-list .list-wrap {
      flex-direction: column;
    }
  }

  @media screen and (min-width: 768px) {
      .videos-list .list-wrap .video {
      flex: 1 0 auto;
      flex-basis: 45%;
      margin: 2vw;
    }
  }

  .videos-list .list-wrap .video-wrap iframe {
    aspect-ratio: 16 / 9;
    width: 100%;
    height: auto;

    /* @media screen and (max-width: 767px) {
      
    }
    @media screen and (max-width: 500px) {
      width: 100%;
      height: auto;
    } */
  }
</style>
<script setup lang="ts">
/**
 * var myData = [];
document.querySelectorAll('#meta #video-title').forEach(video => {
    var id = /v=(.*?)\&list/g.exec(video.getAttribute('href'));
    if (Array.isArray(id)) myData.push({"id": id[1], "href": "https://www.youtube.com/embed/" + id[1], "title":video.innerText, "tags": ["tag", "foo", "bar"]})
})
JSON.stringify(myData)
 */
  const videos = [{
  "id": "pjeaX4Z2N6Q",
  "href": "https://www.youtube.com/embed/pjeaX4Z2N6Q?modestbranding=1&color=white&iv_load_policy=3",
  "title": "[ 𝐖𝐎𝐑𝐊 & 𝐉𝐀𝐙𝐙 ] 作業中に集中力を高めるジャズピアノを演奏💖 Relaxing Jazz Piano Background Music",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "nd5cpmQiP-4",
  "href": "https://www.youtube.com/embed/nd5cpmQiP-4?modestbranding=1&color=white&iv_load_policy=3",
  "title": "Cozy Hobbit Coffee Shop 🍀 Rainy Day at Dreamy Forest with Fireplace For Relax, Study and Sleep",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "fV1kXBfMl6k",
  "href": "https://www.youtube.com/embed/fV1kXBfMl6k?modestbranding=1&color=white&iv_load_policy=3",
  "title": "Ocean - Underwater Ambient Journey - Mysterious Ambient Music For Focus And Concentration",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "l2mW0DxCBY4",
  "href": "https://www.youtube.com/embed/l2mW0DxCBY4",
  "title": "Cozy Coffee Shop Ambience with Relaxing Jazz Music, Rain Sounds and Crackling Fireplace - 8 Hours",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "1R41JB3hbIc",
  "href": "https://www.youtube.com/embed/1R41JB3hbIc",
  "title": "Cozy Winter Ambience with a Soothing Fireplace and the Sound of Gentle Rain",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "vtPpfC1jkiQ",
  "href": "https://www.youtube.com/embed/vtPpfC1jkiQ",
  "title": "Ethereal Horizon: Soothing Sci-Fi Music for a Tranquil Escape",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "SnUBb-FAlCY",
  "href": "https://www.youtube.com/embed/SnUBb-FAlCY",
  "title": "Listen to the rain on the forest path, relax, reduce anxiety, and sleep deeply",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "KIhGy-587Lk",
  "href": "https://www.youtube.com/embed/KIhGy-587Lk",
  "title": "Medieval Fantasy Music - Fantasy Music and Ambience",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "fNnLSCZPXMk",
  "href": "https://www.youtube.com/embed/fNnLSCZPXMk",
  "title": "Peaceful Instrumental Christmas Music - Relaxing Christmas music 'Snowy Christmas Night'",
  "tags": ["tag", "foo", "bar"]
}, {
  "id": "kkNr8c24Xbo",
  "href": "https://www.youtube.com/embed/kkNr8c24Xbo",
  "title": "Staying at the Good Witch's Cabin in the Autumn Forest | ASMR Ambience (musicless) Cats & Herbs",
  "tags": ["tag", "foo", "bar"]
}, 
// {
//   "id": "Nd0beTmpfVA",
//   "href": "https://www.youtube.com/embed/Nd0beTmpfVA",
//   "title": "THE WIZARD'S LIBRARY | MAGICAL FANTASY MUSIC & AMBIENCE",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "q76bMs-NwRk",
//   "href": "https://www.youtube.com/embed/q76bMs-NwRk",
//   "title": "3 Hours of Gentle Night Rain, Rain Sounds for Sleeping - Beat insomnia, Relax, Study, Reduce Stress",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "LfRNadtK0Vw",
//   "href": "https://www.youtube.com/embed/LfRNadtK0Vw",
//   "title": "Music to put you in a better mood 🍀 Chil lofi | Music to Relax, Drive, Study, Chill (4K VIDEO)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "pwvRUR3nlfg",
//   "href": "https://www.youtube.com/embed/pwvRUR3nlfg",
//   "title": "Misty Forest | Celtic Music - Fantasy Magical Harp Music | Rain & Wind Enchanted Forest Ambience",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "QdjXgpmsPCs",
//   "href": "https://www.youtube.com/embed/QdjXgpmsPCs",
//   "title": "'make Dungeon synth great again': a compilation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "oGpGgkByAFI",
//   "href": "https://www.youtube.com/embed/oGpGgkByAFI",
//   "title": "The Cult of the Dead Owl (Ambient).",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "28xY2uji_Cc",
//   "href": "https://www.youtube.com/embed/28xY2uji_Cc",
//   "title": "ANIMAL CROSSING • Relaxed Night Music Compilation🌙",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "MD5o9codaXg",
//   "href": "https://www.youtube.com/embed/MD5o9codaXg",
//   "title": "The Forest Witch Bookshop 📚🔮 Ambience & Soft Music | Collaboration with @noelleburdminiatures3027",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HiG0w4Sw0OU",
//   "href": "https://www.youtube.com/embed/HiG0w4Sw0OU",
//   "title": "Dark Coast - Music and Ambience - Dark Medieval Music for Relaxing",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "3pGwlKjpdfc",
//   "href": "https://www.youtube.com/embed/3pGwlKjpdfc",
//   "title": "Into an Enchanting Forest || Magical Celtic Music @432Hz || Mystical Forest Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "dAsRPFNWOvk",
//   "href": "https://www.youtube.com/embed/dAsRPFNWOvk",
//   "title": "Soothing Mermaid Song for Sleep 🧜‍♀️ Siren's Song & Mermaid Music & Humming (8 HOURS)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "jg9xg6YKXPU",
//   "href": "https://www.youtube.com/embed/jg9xg6YKXPU",
//   "title": "Cozy Christmas Log Cabin Ambience - Relaxing Fireplace and Blizzard Sound for deep sleep",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "NAVj5h0A070",
//   "href": "https://www.youtube.com/embed/NAVj5h0A070",
//   "title": "Harbor Sounds for Sleep, Henningsvær Village Sunrise, Lofoten Norway, 3 Hours",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "0Dk_tgGFQGM",
//   "href": "https://www.youtube.com/embed/0Dk_tgGFQGM",
//   "title": "Octopath Traveler ~ Calm Mix",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ej3MZT3lEs8",
//   "href": "https://www.youtube.com/embed/ej3MZT3lEs8",
//   "title": "Enchanted Forest Music ༄ Relaxing Magical Forest Music 🌳 The Unfading Forest",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "QRMPfEnltdM",
//   "href": "https://www.youtube.com/embed/QRMPfEnltdM",
//   "title": "Employee of The Month - Vaporwave Mix",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "wqYfktcJCfQ",
//   "href": "https://www.youtube.com/embed/wqYfktcJCfQ",
//   "title": "Fantasy Village - Music & Ambience REMASTERED 🧚‍♀️✨",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "AOkuud-rafQ",
//   "href": "https://www.youtube.com/embed/AOkuud-rafQ",
//   "title": "Enchanted Forest Vol.3 Memories From The Past 🧚‍♀️✨",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "O2-Y7Ic530g",
//   "href": "https://www.youtube.com/embed/O2-Y7Ic530g",
//   "title": "WitchCore 🌿Thunderstorm Night in the Forest Cabin / Cats, Herbs, Fireplace and Rain + Soft Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "qEZb-h-juwU",
//   "href": "https://www.youtube.com/embed/qEZb-h-juwU",
//   "title": "Relaxing Night at Rivendell | ASMR Ambience Lord of The Rings & The Hobbit inspired ◈ Sleep/ Relax 🌙",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "WnkV1Ly1HeM",
//   "href": "https://www.youtube.com/embed/WnkV1Ly1HeM",
//   "title": "4K HDR Autumn Waterfall - Stream Sounds - Flowing Water - Forest River - White Noise - Sleep/ Relax",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "IadsLclBOS8",
//   "href": "https://www.youtube.com/embed/IadsLclBOS8",
//   "title": "Autumn Forest - River Sounds - Relaxing Nature Video - White Water - HD - 1080p",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "As_8YRs-Oqk",
//   "href": "https://www.youtube.com/embed/As_8YRs-Oqk",
//   "title": "VICTORIAN AUTUMN ASMR AMBIENCE | Rain & Falling Leaves, Pond Sounds, Horses, Bells, Crunchy Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HZo8CO3YpF4",
//   "href": "https://www.youtube.com/embed/HZo8CO3YpF4",
//   "title": "Autumn Cozy Porch in Forest by the Lake Ambience with Falling Leaves, Birdsong & Water Waves Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "EOzAP96tgE4",
//   "href": "https://www.youtube.com/embed/EOzAP96tgE4",
//   "title": "WitchCore ◈ Autumn Forest 🍂 Good Witch Cabin / Cats, Herbs, Light Rain + Soft Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "6JeZR13dLLI",
//   "href": "https://www.youtube.com/embed/6JeZR13dLLI",
//   "title": "- Folding Space - Generative Modular Ambient // 4 Hour Relaxation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "FuZdbgLiyKw",
//   "href": "https://www.youtube.com/embed/FuZdbgLiyKw",
//   "title": "Rainy Night in Ancient Library - Rain Sounds Helps to Focus on Studying not to be Distracted From",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "WuycU8aFNe8",
//   "href": "https://www.youtube.com/embed/WuycU8aFNe8",
//   "title": "Hogwarts Autumn 🍂 Hagrid's Hut ◈ Harry Potter inspired Ambience / Falling Leaves + Rain showers",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "T7U4VXo-d3w",
//   "href": "https://www.youtube.com/embed/T7U4VXo-d3w",
//   "title": "Lonely Skyrim | The Rift | 2 hrs ambient tour",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "JmkqQw7rdkk",
//   "href": "https://www.youtube.com/embed/JmkqQw7rdkk",
//   "title": "Octopath Traveler ~ Calm Mix II",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "c18WZZa4KIA",
//   "href": "https://www.youtube.com/embed/c18WZZa4KIA",
//   "title": "Fall Coffee Shop Bookstore Ambience with Relaxing Jazz Music & Rain Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "-4hHj38JZpw",
//   "href": "https://www.youtube.com/embed/-4hHj38JZpw",
//   "title": "Tactile Keyboard ASMR | boba u4t | kbd67 lite (no mid-roll ads)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "KBurOperg2c",
//   "href": "https://www.youtube.com/embed/KBurOperg2c",
//   "title": "Severance Wellness Session Music — 8 Hours",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "zmx4Klv6KRY",
//   "href": "https://www.youtube.com/embed/zmx4Klv6KRY",
//   "title": "stillness || stardew valley ost + thunderstorm ambience",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Ox9Tj81KR_A",
//   "href": "https://www.youtube.com/embed/Ox9Tj81KR_A",
//   "title": "Stardew Valley Lullabies - Stardew Valley Overture",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "L3hGIYl_htg",
//   "href": "https://www.youtube.com/embed/L3hGIYl_htg",
//   "title": "ASMR for Anxiety ⛈ Calming Whispers & Guided Visualization for Sleep (Rain & Music Sounds)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Yz2KdHSxGuo",
//   "href": "https://www.youtube.com/embed/Yz2KdHSxGuo",
//   "title": "The Abandoned Greenhouse ◈ ASMR Ambience & Soft Music | Rustling leaves/Wind Howling Relaxing Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "dkswmotS-MA",
//   "href": "https://www.youtube.com/embed/dkswmotS-MA",
//   "title": "Harry Potter Inspired Ambience | Hogwarts Black Lake Boat | Rain Thunderstorm | ASMR",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HlHYOdZePSE",
//   "href": "https://www.youtube.com/embed/HlHYOdZePSE",
//   "title": "Healing Music for Anxiety Disorders, Fears, Depression and Eliminate Negative Thoughts",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "JqpAtf4ygRI",
//   "href": "https://www.youtube.com/embed/JqpAtf4ygRI",
//   "title": "The Hogwarts Express ◈ 6H September 1st Special Train Ride🚂Harry Potter ASMR Ambience | Day to Night",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "hnYt0Eq0P1M",
//   "href": "https://www.youtube.com/embed/hnYt0Eq0P1M",
//   "title": "Harry Potter & Fantastic Beasts | Hogwarts Potions Class Music & Ambience, Collab with ASMR Weekly",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "5wFY5HPZ87A",
//   "href": "https://www.youtube.com/embed/5wFY5HPZ87A",
//   "title": "Pagan Monolith Ambience 🌼🌧️✨ | Witchcraft & Nature | Spring Showers ASMR",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "kmciiBsSmu4",
//   "href": "https://www.youtube.com/embed/kmciiBsSmu4",
//   "title": "Hogwarts Autumn 🍂 [7HOURS] Exploring the castle ◈ Harry Potter inspired Ambience / Rain Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "mU-WiPvxN-I",
//   "href": "https://www.youtube.com/embed/mU-WiPvxN-I",
//   "title": "10 Hours ⚡ HARRY POTTER ASMR Ambience ⋄ Hogwarts, The burrow, Privet drive & More ✨ Relax & Study 📚",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "1H0JKfZD24M",
//   "href": "https://www.youtube.com/embed/1H0JKfZD24M",
//   "title": "Hogwarts Library 📚 POMODORO Study Session 25/5 - Harry Potter Ambience 📚 Focus, Relax & Study",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "rv0CqEYnJV0",
//   "href": "https://www.youtube.com/embed/rv0CqEYnJV0",
//   "title": "Forest of Dean ◈ Winter ASMR | Relaxing Howling Wind | Harry Potter inspired Ambience & Soft Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "zJW0NG6BYkY",
//   "href": "https://www.youtube.com/embed/zJW0NG6BYkY",
//   "title": "Rainy day in the Greenhouse ◈ Cottage Core Aesthetic ASMR Ambience ◈ Nature Sounds ◈ Soft Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "gz-SCxj8rds",
//   "href": "https://www.youtube.com/embed/gz-SCxj8rds",
//   "title": "🦋THE BUTTERFLY EFFECT ⁂ Elevate your Vibration ⁂ Positive Aura Cleanse ⁂ 432Hz Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "KDJjrRVik5o",
//   "href": "https://www.youtube.com/embed/KDJjrRVik5o",
//   "title": "Heavy Rain In Victorian London | Rain On Window | Fall Asleep Fast | Sleep Well | 4K | 8 Hours",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HWlrP4w0uRo",
//   "href": "https://www.youtube.com/embed/HWlrP4w0uRo",
//   "title": "Hogsmeade Window 'Winter Night' ⛄ Harry potter ASMR Ambience - Christmas Music 🎄 Fireplace & Snow",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "UPC5skXme10",
//   "href": "https://www.youtube.com/embed/UPC5skXme10",
//   "title": "Winter Enchanted Forest Night Ambience 🍄❄️Occasional Snowfall, Soothing Chimes & Mystical Atmosphere",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "10P52OzMwTc",
//   "href": "https://www.youtube.com/embed/10P52OzMwTc",
//   "title": "Haunted Village Halloween Ambience 🦇 3 Hours of Relaxing Spooky and Fall Nature Sounds, White Noise",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "WBLTQYl_dXQ",
//   "href": "https://www.youtube.com/embed/WBLTQYl_dXQ",
//   "title": "3 hours of relaxing nintendo music | cosmic",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "__vGDrXN3VQ",
//   "href": "https://www.youtube.com/embed/__vGDrXN3VQ",
//   "title": "cozy autumn nintendo mix 🍁",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "PszSx4HvKAA",
//   "href": "https://www.youtube.com/embed/PszSx4HvKAA",
//   "title": "Tibetan Music, Healing Music, Relaxation Music, Chakra, Relaxing Music for Stress Relief, ✿3193C",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Pa_s7ogtokM",
//   "href": "https://www.youtube.com/embed/Pa_s7ogtokM",
//   "title": "Relaxing Minecraft Music (Extended Mix.)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HoAsuHnmdUg",
//   "href": "https://www.youtube.com/embed/HoAsuHnmdUg",
//   "title": "The Lord of the Rings: Bilbo’s Study Ambience & Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "bl_eV3MqOwI",
//   "href": "https://www.youtube.com/embed/bl_eV3MqOwI",
//   "title": "Austria 4K Nature Relaxation Film | Beautiful Relaxing Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "FIMdEPd98xs",
//   "href": "https://www.youtube.com/embed/FIMdEPd98xs",
//   "title": "INSOMNIA RELIEF [Fall Asleep Fast] 'The Blue Forest' Binaural Beats Sleep Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "h_ORaOxOe8I",
//   "href": "https://www.youtube.com/embed/h_ORaOxOe8I",
//   "title": "Sleeping Music for DEEP SLEEPING [2,6Hz Delta Waves] Binaural Beats Sleep Healing",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ox1xHrMLOyk",
//   "href": "https://www.youtube.com/embed/ox1xHrMLOyk",
//   "title": "Peaceful Campfire at Sunrise - 5K Nature Relaxation Video with Crackling Fire Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "lR4GNWcwAI8",
//   "href": "https://www.youtube.com/embed/lR4GNWcwAI8",
//   "title": "Forest Creek Sounds | 3 Hours | Sleep, Relax, Focus or Meditation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "LYF2VzCN0os",
//   "href": "https://www.youtube.com/embed/LYF2VzCN0os",
//   "title": "Cozy Camp in Eerie Forest | Campfire and Spooky Woods Sounds ・ Soundscape Ambience for D&D || RDR2",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "4LeyBbDBvQQ",
//   "href": "https://www.youtube.com/embed/4LeyBbDBvQQ",
//   "title": "8 HOURS of Incredibly Calming Sound of Rain and Birds Chirping in the Forest (4K UltraHD)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "CN_yZr2T2wU",
//   "href": "https://www.youtube.com/embed/CN_yZr2T2wU",
//   "title": "Morning Lake - 8 HOURS of Water Lapping the Lake Shore - Nature Relaxation Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "0ANLBX2EgmM",
//   "href": "https://www.youtube.com/embed/0ANLBX2EgmM",
//   "title": "8 HOURS of Fascinating Sunset over the Tropical Beach with Calming Waves Sounds (4K UHD)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "gwE5dGJ_KI0",
//   "href": "https://www.youtube.com/embed/gwE5dGJ_KI0",
//   "title": "8 HOURS Tranquil Birdsong on Calm Fall Lake - Nature Soundscapes 4K Video",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "sX6J4t2lRu0",
//   "href": "https://www.youtube.com/embed/sX6J4t2lRu0",
//   "title": "8 HOURS Calm Ocean Waves Sounds - Tropical Beach Sunrise 4K Video",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "qRTVg8HHzUo",
//   "href": "https://www.youtube.com/embed/qRTVg8HHzUo",
//   "title": "8 Hours of Birds Singing on the Lakeshore and Water Sounds - Relaxing Nature Sounds - Mount Shuksan",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "cAbJtTxU56E",
//   "href": "https://www.youtube.com/embed/cAbJtTxU56E",
//   "title": "8 Hours Nighttime Ambience - 4K Grand Teton and Milky Way - Nature soundscapes",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Q-sZipetAEc",
//   "href": "https://www.youtube.com/embed/Q-sZipetAEc",
//   "title": "10 HRS of Nighttime Nature Soundscapes (Lake Waves, Cicadas, Crickets) - 8K Enchanting Night",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "4bRxLVSfHPU",
//   "href": "https://www.youtube.com/embed/4bRxLVSfHPU",
//   "title": "romantic hotel ambience where you can see the aurora",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "XJ_ZKQcRIEg",
//   "href": "https://www.youtube.com/embed/XJ_ZKQcRIEg",
//   "title": "European Modern Era Private library Ambience",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "E2_sgElGys4",
//   "href": "https://www.youtube.com/embed/E2_sgElGys4",
//   "title": "Rain & Thunderstorm Sounds | Rainstorm with Lightning Thunder for Sleeping, Focus and Relaxation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "PrSXb44xu0s",
//   "href": "https://www.youtube.com/embed/PrSXb44xu0s",
//   "title": "- Submerged - | Ocean Ambient Music | Underwater Sounds 🤿",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "_v4cgUVBsi4",
//   "href": "https://www.youtube.com/embed/_v4cgUVBsi4",
//   "title": "Hogwarts Great Hall | Harry Potter Music & Ambience",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "3DTvk8boR8U",
//   "href": "https://www.youtube.com/embed/3DTvk8boR8U",
//   "title": "The Lord of the Rings: Bag End Ambience & Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "dx3GxpitvbY",
//   "href": "https://www.youtube.com/embed/dx3GxpitvbY",
//   "title": "Coffee Shop Ambience ☕Cozy Rainy Day [ASMR Study & Relax] keyboard typing + Light Rain + people",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HA2LTXOUMzM",
//   "href": "https://www.youtube.com/embed/HA2LTXOUMzM",
//   "title": "Enter The Astral Realm | 432 Hz Deep Lucid Dreaming Sleep Music | 8 Hz Binaural Beat Brainwaves",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "fe5Vo9U0FJE",
//   "href": "https://www.youtube.com/embed/fe5Vo9U0FJE",
//   "title": "🎧 Rain on window at night-Night City View 10 Hours Relaxation and Sleep | Cozy bedroom | Study",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "npVellnR6D8",
//   "href": "https://www.youtube.com/embed/npVellnR6D8",
//   "title": "Twin Peaks Double R Diner Ambience - 8 Hours of Smooth Jazz Music, Rain Sounds, & Cozy Cafe Ambience",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "g1w3IT5WnYw",
//   "href": "https://www.youtube.com/embed/g1w3IT5WnYw",
//   "title": "Night Ambient Sounds, Cricket, Swamp Sounds at Night, Sleep and Relaxation Meditation Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "dTKFt0YyEFQ",
//   "href": "https://www.youtube.com/embed/dTKFt0YyEFQ",
//   "title": "😴🔥❄ Crackling Fire & Blizzard Storm Sounds Outside | 10 Hours for Insomnia, Sleep, Relaxation, Spa",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "mA5THpy0zsg",
//   "href": "https://www.youtube.com/embed/mA5THpy0zsg",
//   "title": "4K HDR Enchanted Forest - Blackbird Singing - Springtime Bird Song - Relaxing Nature Video & Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "XxP8kxUn5bc",
//   "href": "https://www.youtube.com/embed/XxP8kxUn5bc",
//   "title": "4K Forest Birdsong 2 - Birds Sing in the Woods - No Loop Realtime Birdsong - Relaxing Nature Video",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "6oD1uYkbc9Y",
//   "href": "https://www.youtube.com/embed/6oD1uYkbc9Y",
//   "title": "🎄⛄ Christmas JAZZ songs instrumental playlist / Carol Jazz Piano Collection",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "AWKzr6n0ea0",
//   "href": "https://www.youtube.com/embed/AWKzr6n0ea0",
//   "title": "🔥 The Best 4K Relaxing Fireplace with Crackling Fire Sounds 8 HOURS No Music 4k UHD TV Screensaver",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "l-yyCItiToQ",
//   "href": "https://www.youtube.com/embed/l-yyCItiToQ",
//   "title": "Classic Christmas & Holiday HD Yule Log Fireplace - Feat. 90 Mins Of Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "j9hR4Gg6b9w",
//   "href": "https://www.youtube.com/embed/j9hR4Gg6b9w",
//   "title": "Kmart In-Store Music: Christmas 1974 (reupload/recreation)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "mmJ-KiSIsD4",
//   "href": "https://www.youtube.com/embed/mmJ-KiSIsD4",
//   "title": "🎅🎄⛄ Happy ver. Christmas Jazz instrumental / Carol Piano Collection",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "iGwawktAMRg",
//   "href": "https://www.youtube.com/embed/iGwawktAMRg",
//   "title": "4K Relaxing Fireplace & The Best Instrumental Christmas Music & Crackling Fire Sounds 🔥 UHD 2 Hours",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "7smahC_IAiY",
//   "href": "https://www.youtube.com/embed/7smahC_IAiY",
//   "title": "1 Hour Relaxing Harry Potter Winter/Christmas Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "NT5JUfO2JlI",
//   "href": "https://www.youtube.com/embed/NT5JUfO2JlI",
//   "title": "Relaxing Dragon Quest Music Compilation - Symphonic Suites",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "HfR_EDFvrLc",
//   "href": "https://www.youtube.com/embed/HfR_EDFvrLc",
//   "title": "4K HDR Autumn Cascade - Waterfall Sounds - White Water - Relaxing Forest Ambiance Video",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "6zGQSWib32E",
//   "href": "https://www.youtube.com/embed/6zGQSWib32E",
//   "title": "10 Hours of Relaxing Sleep Music With Black Screen After 1 Hour",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "KmdbqI9Aa8o",
//   "href": "https://www.youtube.com/embed/KmdbqI9Aa8o",
//   "title": "Destiny Ambience - Ocean of Storms, Archers Line",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "y1wegnxW5dM",
//   "href": "https://www.youtube.com/embed/y1wegnxW5dM",
//   "title": "Destiny Ambience - Venus, Ishtar Sink, Maat Mons (4k)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "md_WC9vdNp8",
//   "href": "https://www.youtube.com/embed/md_WC9vdNp8",
//   "title": "Destiny Ambience - Cosmodrome, Old Russia (Walls)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "2G8LAiHSCAs",
//   "href": "https://www.youtube.com/embed/2G8LAiHSCAs",
//   "title": "Forest Birdsong Nature Sounds-Relaxing Bird Sounds for Sleeping-Calming Birds Chirping Ambience",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "SLgms78JVo0",
//   "href": "https://www.youtube.com/embed/SLgms78JVo0",
//   "title": "3 Hours of Relaxing Super Nintendo Music - SNESdrunk",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "lpNgST3RX4Q",
//   "href": "https://www.youtube.com/embed/lpNgST3RX4Q",
//   "title": "Deep Relaxing Music, Vol. 1 - Ambient Music for Sleep, Meditation, Focus & Relaxation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "PxnegJdRnUg",
//   "href": "https://www.youtube.com/embed/PxnegJdRnUg",
//   "title": "Soothing Soundscape for Insomnia Relief",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "eKmRkS1os7k",
//   "href": "https://www.youtube.com/embed/eKmRkS1os7k",
//   "title": "Sleep and Relaxation Nature Sounds, Crickets Summer Night - Sleep Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "239d5JM161Q",
//   "href": "https://www.youtube.com/embed/239d5JM161Q",
//   "title": "8 Hours Nature Sounds Woodland Birds Chriping-Relaxing Spring Birdsong Ambience-Forest Birds Singing",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "-zWS52fBtSE",
//   "href": "https://www.youtube.com/embed/-zWS52fBtSE",
//   "title": "Summer Night Sounds for Sleeping 10 Hours with Crickets",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "KsMqhVfUC9w",
//   "href": "https://www.youtube.com/embed/KsMqhVfUC9w",
//   "title": "417 Hz Healing music | Let go of mental blockages, Remove negative energy, Healing frequency music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Qh7ICKRgFW8",
//   "href": "https://www.youtube.com/embed/Qh7ICKRgFW8",
//   "title": "Horizon Zero Dawn: Ambient Music Compilation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "H1iboKia3AQ",
//   "href": "https://www.youtube.com/embed/H1iboKia3AQ",
//   "title": "4K Spring Forest - Blackbird Song - Bird Singing/ Chirping - Ultra HD Relaxing Nature Video & Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ftlvreFtA2A",
//   "href": "https://www.youtube.com/embed/ftlvreFtA2A",
//   "title": "FLYING OVER NORWAY (4K UHD) 1HR Ambient Drone Film + Music by Nature Relaxation™ for Stress Relief",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "FjU_x1106pg",
//   "href": "https://www.youtube.com/embed/FjU_x1106pg",
//   "title": "MANHATTAN | NEW YORK CITY - NY , UNITED STATES - A TRAVEL TOUR - UHD 4K",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Ftm2uv7-Ybw",
//   "href": "https://www.youtube.com/embed/Ftm2uv7-Ybw",
//   "title": "4K Campfire by the River - Relaxing Fireplace & Nature Sounds - Robin Birdsong - UHD Video - 2160p",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "9lh_becOt4Y",
//   "href": "https://www.youtube.com/embed/9lh_becOt4Y",
//   "title": "4K Campfire by the Sea - Crickets & Ocean Waves - Night Forest Nature Sounds - Relaxing Fireplace",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Ux8xAuQBdkk",
//   "href": "https://www.youtube.com/embed/Ux8xAuQBdkk",
//   "title": "4K Realtime Fireplace - Relaxing Fire Burning Video - 3 Hours - No Loop - Ultra HD - 2160p",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "IsPBplWLImI",
//   "href": "https://www.youtube.com/embed/IsPBplWLImI",
//   "title": "4K HDR Bluebell Woods - English Forest - Birds Singing - No Loop - Relaxing Nature Video & Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "xSnulMePm_8",
//   "href": "https://www.youtube.com/embed/xSnulMePm_8",
//   "title": "BiNaural Beats Study Music - Improve Memory and Concentration",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Kt7jjEAWPds",
//   "href": "https://www.youtube.com/embed/Kt7jjEAWPds",
//   "title": "Happiness Frequency - Serotonin, Dopamine and Endorphin Release ☯3325",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ksrnQ7i82T0",
//   "href": "https://www.youtube.com/embed/ksrnQ7i82T0",
//   "title": "Chillin' with Inner Ocean Records · jazzy hip hop mix",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "kwLTw8F8yN8",
//   "href": "https://www.youtube.com/embed/kwLTw8F8yN8",
//   "title": "Waves - A Chillwave Mix",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "xNN7iTA57jM",
//   "href": "https://www.youtube.com/embed/xNN7iTA57jM",
//   "title": "Forest Sounds | Woodland Ambience, Bird Song",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "4zqKJBxRyuo",
//   "href": "https://www.youtube.com/embed/4zqKJBxRyuo",
//   "title": "Instant Calm, Beautiful Relaxing Sleep Music, Dream Music (Nature Energy Healing, Quiet Ocean) ★11",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "mIYzp5rcTvU",
//   "href": "https://www.youtube.com/embed/mIYzp5rcTvU",
//   "title": "Classical Music for Reading - Mozart, Chopin, Debussy, Tchaikovsky...",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "MyitVNMFApc",
//   "href": "https://www.youtube.com/embed/MyitVNMFApc",
//   "title": "Blade Runner Meditative Ambience with City Sounds",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ncjuqj0WN6s",
//   "href": "https://www.youtube.com/embed/ncjuqj0WN6s",
//   "title": "Instrumental Christmas Music • Piano Covers of Traditional Christmas Songs",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "5tXht-NGmc0",
//   "href": "https://www.youtube.com/embed/5tXht-NGmc0",
//   "title": "New York Jazz Lounge - Merry Christmas",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "kRXrqURyRy0",
//   "href": "https://www.youtube.com/embed/kRXrqURyRy0",
//   "title": "Instrumental Christmas Music with Fireplace 24/7 - Merry Christmas!",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "74b3Zb18UDM",
//   "href": "https://www.youtube.com/embed/74b3Zb18UDM",
//   "title": "Go to Sleep with Thunder & Rain Sounds | Relaxing Sounds for Insomnia Symptoms & Sleeping Disorders",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "WZKW2Hq2fks",
//   "href": "https://www.youtube.com/embed/WZKW2Hq2fks",
//   "title": "3 Hour Zen Meditation Music: Nature Sounds, Relaxing Music, Calming Music, Healing Music, ✿071C",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "1ZYbU82GVz4",
//   "href": "https://www.youtube.com/embed/1ZYbU82GVz4",
//   "title": "Relaxing Sleep Music • Deep Sleeping Music, Relaxing Music, Stress Relief, Meditation Music (Flying)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "4vIQON2fDWM",
//   "href": "https://www.youtube.com/embed/4vIQON2fDWM",
//   "title": "Library Sounds | Study Ambience | 2 hours",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "7pmxO9fHBHk",
//   "href": "https://www.youtube.com/embed/7pmxO9fHBHk",
//   "title": "Activate Your Higher Mind for Success ☯ Subconscious Mind Programming ☯ Mind/Body Integration",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "3sL0omwElxw",
//   "href": "https://www.youtube.com/embed/3sL0omwElxw",
//   "title": "Rain & Thunderstorm Sounds | Crackling Fireplace | 3 hours",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ayXQdXF-338",
//   "href": "https://www.youtube.com/embed/ayXQdXF-338",
//   "title": "Destiny - Main Menu Music - 1 hour",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "AKvZPdVctAs",
//   "href": "https://www.youtube.com/embed/AKvZPdVctAs",
//   "title": "12 Hrs - Ocean Waves, Sounds Nature, Relaxation, Yoga, Meditation, Reading, Sleep, Study",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "QV88lLoAbow",
//   "href": "https://www.youtube.com/embed/QV88lLoAbow",
//   "title": "Relaxation Music,Chakra,stress reduction music, background music ✿1",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "GLeXLoiZHnc",
//   "href": "https://www.youtube.com/embed/GLeXLoiZHnc",
//   "title": "Relaxing Celtic Music: Beautiful Relaxing Music, Meditation Music, celtic flute",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "od2F6SrG9Cc",
//   "href": "https://www.youtube.com/embed/od2F6SrG9Cc",
//   "title": "8 Hrs Best Celtic Music: Beautiful Music, Relaxing Music, Flute Music, Meditation Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "Aeh-c6QfWuw",
//   "href": "https://www.youtube.com/embed/Aeh-c6QfWuw",
//   "title": "Native American Indian Music | Power Animals & Native Nights | Shaman soft sleep music | Niall",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "ilBDzoV1Z6s",
//   "href": "https://www.youtube.com/embed/ilBDzoV1Z6s",
//   "title": "Relaxing Music - Positive Feelings and Energy - Relax Mind Body, Healing Music",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "s0mI6TH8Wh0",
//   "href": "https://www.youtube.com/embed/s0mI6TH8Wh0",
//   "title": "12 Hours Thunder and soft rain - nature sound for sleep, study, relaxation",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "OE69ckQnkRA",
//   "href": "https://www.youtube.com/embed/OE69ckQnkRA",
//   "title": "Healing Music for Meditation, Music for Stress Relief, Yoga, Spa, Massage 4K",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "1Y4ueraP6H8",
//   "href": "https://www.youtube.com/embed/1Y4ueraP6H8",
//   "title": "Healing Music for Stress Relief, Relaxing Music, Meditation, Massage, Yoga & SPA",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "RuZyYAtNIoI",
//   "href": "https://www.youtube.com/embed/RuZyYAtNIoI",
//   "title": "Destiny Chill Music Collection (25 minutes)",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "nn3wvAN15Ys",
//   "href": "https://www.youtube.com/embed/nn3wvAN15Ys",
//   "title": "4K Autumn Meditation - UHD Beautiful Nature Video & Relaxing MUSIC - Forest River Sounds - 1h 2160p",
//   "tags": ["tag", "foo", "bar"]
// }, {
//   "id": "fW-mixqTTwE",
//   "href": "https://www.youtube.com/embed/fW-mixqTTwE",
//   "title": "(3 hours) 4K UHD Relaxation video: Mount Rainier National Park Washington State, Nature Sounds - 1",
//   "tags": ["tag", "foo", "bar"]
// }
]
</script>