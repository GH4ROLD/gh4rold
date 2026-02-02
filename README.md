### Hi there, I'm Harold Justiniano 👋
#### 🔊 Technical Audio Designer | Composer | Unity Developer

I bridge the gap between **Musical Artistry** and **Game Logic**. 
As a **Music Professor** turned **Game Audio Developer** based in Chile 🇨🇱, I specialize in designing immersive adaptive audio systems and implementing them directly into game engines.

- 🔭 **Current Focus:** Developing a dynamic audio system for a psychological horror game using **Wwise + Godot**.
- 💡 **Core Philosophy:** Audio shouldn't just be heard; it should react to gameplay.

---

### 🛠️ Technical Arsenal

| **Game Engines** | **Audio Middleware & DAW** | **Tools & Scripting** |
| :--- | :--- | :--- |
| ![Godot Engine](https://img.shields.io/badge/Godot_4.x-%23FFFFFF.svg?style=flat&logo=godot-engine&logoColor=478cbf) | ![Wwise](https://img.shields.io/badge/Wwise-Learning-yellow?style=flat) | ![GDScript](https://img.shields.io/badge/GDScript-478cbf?style=flat&logo=godot-engine&logoColor=white) |
| ![Unreal Engine](https://img.shields.io/badge/Unreal_5-Learning-black?style=flat&logo=unrealengine&logoColor=white) | ![Reaper](https://img.shields.io/badge/REAPER-Scripting-1155cc?style=flat&logo=reaper&logoColor=white) | ![Git](https://img.shields.io/badge/Git-%23F05033.svg?style=flat&logo=git&logoColor=white) |

---

### 🚀 Selected Projects

| Project | Role | Audio Tech Stack |
| :--- | :--- | :--- |
| **Global Game Jam 2026 Entry** | *Technical Audio Lead* | Godot 4 • Adaptive Music Layers |
| **Psychological Horror Title** *(In Development)* | *Sound Designer / Implementer* | Godot 4 • Wwise • Spatial Audio |
| **Exotico Records** | *Co-Founder / Producer* | Label Management • Lofi Production |

---

### 💻 Implementation Showcase: Adaptive Audio in Godot

I write clean, modular GDScript to handle complex audio transitions. Here is a snippet of a **Dynamic Music Manager** using Tweens for smooth crossfading based on game states:

```gdscript
extends Node

const FADE_TIME: float = 2.0
const VOL_ON: float = 0.0
const VOL_OFF: float = -80.0

# Switches track layers based on gameplay intensity (Exploration vs Combat)
func set_music_state(state: String) -> void:
	var tween = create_tween().set_parallel(true)
	
	match state:
		"COMBAT":
			# Smoothly bring in percussion/high energy layers
			tween.tween_property($Layers/Percussion, "volume_db", VOL_ON, FADE_TIME)
			tween.tween_property($Layers/Ambience, "volume_db", -10.0, FADE_TIME)
		"EXPLORATION":
			# Revert to ambient textures
			tween.tween_property($Layers/Percussion, "volume_db", VOL_OFF, FADE_TIME)
			tween.tween_property($Layers/Ambience, "volume_db", VOL_ON, FADE_TIME)
