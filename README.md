### Hi there, I'm Harold Justiniano 👋
#### 🔊 Sound Designer | Composer | Technical Audio Implementer

I bridge the gap between **Musical Artistry** and **Game Logic**. 
As a **Music Professor** turned **Game Audio Developer** based in Chile 🇨🇱, I specialize in designing immersive soundscapes and implementing them using **Unity** and middleware.

- 🔭 **Current Focus:** Pre-production for the psychological horror title **"BLIND FAITH"**.
- 💡 **Core Philosophy:** Audio shouldn't just be heard; it should react to gameplay.

---

### 🛠️ Technical Arsenal

| **Game Engines & Language** | **Audio Middleware & DAW** | **Version Control** |
| :--- | :--- | :--- |
| ![Unity](https://img.shields.io/badge/Unity-2022.x-black?style=flat&logo=unity&logoColor=white) | ![Ableton](https://img.shields.io/badge/Ableton_Live-11-black?style=flat&logo=abletonlive&logoColor=white) | ![Git](https://img.shields.io/badge/Git-%23F05033.svg?style=flat&logo=git&logoColor=white) |
| ![C#](https://img.shields.io/badge/C%23-Scripting-239120?style=flat&logo=c-sharp&logoColor=white) | ![Wwise](https://img.shields.io/badge/Wwise-Middleware-blue?style=flat) | ![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat&logo=github&logoColor=white) |

---

### 🚀 Projects

| Project | Genre | Status | Role |
| :--- | :--- | :--- | :--- |
| **BLIND FAITH** | Psychological Horror | *Pre-production* | **Audio Director / Technical Sound Designer**<br>Designing adaptive audio systems for horror atmosphere. |

---

### 💻 Implementation Showcase: C# Audio Logic

I write clean, modular **C#** scripts in Unity to handle dynamic audio changes. Here is an example of how I structure a music state manager:

```csharp
using UnityEngine;

public class DynamicMusicManager : MonoBehaviour
{
    [Header("Audio Configurations")]
    [SerializeField] private float fadeDuration = 2.0f;
    
    // Example: Switching music intensity based on Player State
    public void SetMusicState(string stateName)
    {
        switch (stateName)
        {
            case "CHASE":
                // Trigger high intensity layers / Wwise State
                Debug.Log("Audio: Transitioning to CHASE state.");
                // AkSoundEngine.SetState("Music_State", "Chase"); 
                break;

            case "EXPLORE":
                // Revert to ambient textures
                Debug.Log("Audio: Transitioning to EXPLORE state.");
                // AkSoundEngine.SetState("Music_State", "Explore");
                break;
        }
    }
}
