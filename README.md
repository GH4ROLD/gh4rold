### Hi there, I'm Harold Justiniano 👋
#### Composer | Sound Designer | Technical Audio Implementer

I am a **Music Professor** turned **Game Audio Developer** from Chile. I specialize in creating immersive soundscapes and implementing them directly into game engines, bridging the gap between art and code.

- 🔭 I’m currently working on: **Global Game Jam 2026 Project**
- 🌱 I’m currently learning: **Wwise Middleware & Unreal Engine 5**
- 🎮 Engine of choice: **Godot 4.x**
- 🎵 Main Genre: **Lofi / Bossa Nova / Ambient**

---

### 🛠️ Tech Stack & Tools

![Godot Engine](https://img.shields.io/badge/GODOT-%23FFFFFF.svg?style=for-the-badge&logo=godot-engine&logoColor=478cbf)
![Reaper](https://img.shields.io/badge/REAPER-1155cc?style=for-the-badge&logo=reaper&logoColor=white)
![Wwise](https://img.shields.io/badge/Wwise-Learning-yellow?style=for-the-badge)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GDScript](https://img.shields.io/badge/GDScript-478cbf?style=for-the-badge&logo=godot-engine&logoColor=white)

---

### 🎧 Implementation Showcase

Here is how I organize my audio logic in Godot:

```gdscript
# Example of how I handle Dynamic Music transitions
func change_music_intensity(intensity_level):
    var tween = create_tween()
    if intensity_level == "High":
        tween.tween_property($MusicPlayer/BattleLayer, "volume_db", 0.0, 1.0)
        tween.tween_property($MusicPlayer/CalmLayer, "volume_db", -80.0, 1.0)
    else:
        tween.tween_property($MusicPlayer/BattleLayer, "volume_db", -80.0, 1.0)
        tween.tween_property($MusicPlayer/CalmLayer, "volume_db", 0.0, 1.0)
