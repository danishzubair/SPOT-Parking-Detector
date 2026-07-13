# SPOT – AI Parking Space Availability Monitor

> **Never miss your street parking space again.**

SPOT is an AI-powered parking monitoring system designed specifically for one of the biggest daily frustrations faced by people living in **terraced houses across the UK** — waiting for a parking space outside their home.

Instead of constantly checking through the window every few minutes, SPOT watches the parking space for you and immediately alerts you the moment it becomes available.

When the parked car leaves, **SPOT automatically beeps five times**, giving you enough time to grab your keys and park before someone else does.

---

## The Problem

If you live on a busy residential street, you've probably experienced this:

- You come home from work.
- There are no parking spaces outside your house.
- You park several streets away.
- You spend the next hour repeatedly looking out the window hoping someone leaves.
- Someone else gets the space before you notice.

SPOT solves exactly this problem.

---

# Features

## Live Camera Monitoring

Uses your webcam or external camera to continuously monitor a parking space in real time.

---

## Draw Your Own Parking Zone

Every street is different.

Simply:

1. Enable the camera
2. Click and drag over the parking space you want to monitor
3. Capture the spot while it's empty
4. Start monitoring

No complicated setup.

---

## Reference Capture

SPOT captures multiple frames of the **empty parking space** and creates a clean reference image.

This reference is then used to compare future frames.

---

## AI Vehicle Classification

Unlike simple motion detection systems, SPOT uses an AI classification system to determine what is actually inside the selected parking area.

It can distinguish between:

- Cars
- Vans
- People walking through
- Shadows
- Temporary movement

This dramatically improves detection accuracy by reducing unnecessary alerts caused by random movement.

---

## Live Parking Status

The monitored parking area is drawn directly on the video feed.

### Occupied

- Red outline
- "Occupied" label
- Live confidence score

### Available

- Green outline
- "Clear" label

Everything updates live.

---

## Instant Audio Alerts

The moment a previously occupied parking space becomes empty:

SPOT immediately plays **5 loud beeps**

This allows you to react before someone else parks there.

Importantly:

SPOT **does NOT beep** if the space is already empty when monitoring begins.

It only alerts when:

```
Occupied -> Empty
```

This prevents unnecessary notifications.

---

## Adjustable Detection Threshold

Every street is different.

Rain.

Fog.

Changing sunlight.

Tree shadows.

Headlights.

Because of this, SPOT allows the user to adjust the detection sensitivity using the **Threshold** slider.

Lower threshold:

- More sensitive
- Detects smaller changes
- Higher chance of false positives

Higher threshold:

- Less sensitive
- Ignores small environmental changes
- More stable

A built-in guide explains exactly how to calibrate it for the best results.

---

## Live Detection Statistics

SPOT displays useful monitoring information including:

- Detection count
- Current confidence
- Difference score
- Zone size
- Session uptime
- Reference capture time
- Camera status

---

## 60-Second History Timeline

A live history graph shows the last 60 seconds of parking activity.

This allows users to quickly see:

- When vehicles arrived
- When vehicles left
- Detection confidence
- Threshold position

Great for debugging and calibration.

---

## Comprehensive Event Logs

Every important event is recorded.

Examples:

- Camera started
- Zone drawn
- Reference captured
- Vehicle detected
- Parking space became available
- Alert triggered
- Camera stopped

This makes it easy to understand exactly what the system is doing.

---

## Lightweight

SPOT is distributed as a **single standalone HTML file**.

No installation.

No IDE required.

No additional libraries.

No cloud services.

No subscriptions.

No accounts.

Simply download **`SPOT.html`**, double-click to open it in your web browser, **allow camera access**, and start monitoring within seconds.

---

# How It Works

```text
Enable Camera
      ↓
Draw Parking Zone
      ↓
Capture Empty Space
      ↓
Start Monitoring
      ↓
Vehicle Arrives
      ↓
Zone Becomes Occupied
      ↓
Vehicle Leaves
      ↓
SPOT Detects Empty Space
      ↓
Beep ×5
```

---

# Detection Pipeline

SPOT combines traditional computer vision techniques with AI-assisted classification.

The monitoring pipeline includes:

- Live webcam capture
- User-defined region of interest (ROI)
- Multi-frame reference averaging
- Image preprocessing
- Grayscale conversion
- Blur filtering
- Brightness normalization
- Difference scoring
- Confidence smoothing
- Adaptive background learning
- AI object classification
- Occupancy decision
- Audio alert generation

This layered approach helps reduce false detections compared to simple frame differencing.

---

# Limitations

Real-world environments are unpredictable.

Performance may be affected by:

- Heavy rain
- Dense fog
- Night-time glare
- Strong shadows
- Camera movement
- Vehicles partially covering the parking space
- Large pedestrians standing inside the monitored zone

For this reason, users are encouraged to fine-tune the **Threshold** slider for their environment.

---

# Best Results

For the highest accuracy:

- Mount the camera securely.
- Avoid camera shake.
- Draw the parking zone tightly around the parking space.
- Capture the reference only when the space is completely empty.
- Re-capture the reference if lighting changes dramatically.
- Keep the lens clean.

---

# Future Improvements

Planned features include:

- Mobile notifications
- SMS alerts
- Smartwatch notifications
- Multiple parking space monitoring
- YOLOv8 vehicle detection
- License plate recognition
- Night vision optimisation
- Automatic threshold calibration
- Remote monitoring
- Historical analytics dashboard
- Raspberry Pi deployment
- Cloud event logging

---

# Who Is This For?

SPOT is perfect for:

- People living in terraced houses
- Busy residential streets
- Limited on-street parking
- Shared parking areas
- Residents tired of checking outside every few minutes

---

# Why SPOT?

Every day, thousands of UK residents lose the parking space outside their home simply because they didn't notice it becoming free.

SPOT watches for you.

No more standing at the window.

No more constantly refreshing CCTV feeds.

No more missing the perfect parking opportunity by seconds.

Just a simple beep at exactly the right moment.

---

## If you found this project interesting, please consider giving it a star and share it with others!

It helps others discover the project and motivates future development.
