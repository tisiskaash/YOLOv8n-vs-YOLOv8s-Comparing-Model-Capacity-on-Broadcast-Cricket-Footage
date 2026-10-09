# YOLOv8n-vs-YOLOv8s-Comparing-Model-Capacity-on-Broadcast-Cricket-Footage
YOLOv8n vs YOLOv8s
---

**Step 1:** Open this notebook in Google Colab 
**Step 2:** Enable GPU — Runtime → Change runtime type → **T4 GPU** 
**Step 3:** Get a free Roboflow API key:
- Go to https://roboflow.com → Sign up (free)
- Go to Settings → API Keys → copy your key
- Paste it in Section 2 where it says `ROBOFLOW_API_KEY = "YOUR_KEY_HERE"`

**Step 4:** Runtime → Run all 
**Expected runtime:** ~25–40 minutes on T4 GPU

---

## Project Overview

This project implements real-time cricket scene understanding using object detection.
We detect 6 object classes from live broadcast cricket footage:
- **batsman** — the player currently batting
- **bowler** — the player delivering the ball
- **umpire** — match official on the field
- **wicket keeper** — fielder behind the stumps
- **ball** — the cricket ball (small, fast-moving, hardest class)
- **stumps** — the three vertical posts at each end

**Real-world application:** This system directly underpins broadcast AI for automated
player tracking, DRS (Decision Review System) assistance, and smart highlight generation
used by broadcasters like Sky Sports and Star Sports.

**Comparison:** YOLOv8n (nano, 3.2M params) vs YOLOv8s (small, 11.2M params)
— same architecture family, different model capacity. This lets us directly measure
the accuracy/speed tradeoff at the two smallest viable scales for real-time deployment.
