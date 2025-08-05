# PHANTOM-OS DATAGLOVE RAG-DRIVERS  
**Build your own virtual drivers for DATAGLOVES to manage PC Visual Systems** 

#like the modern graphics systems virtual drivers by phantom-os datagloves

![PHANTOM OS DATAGLOVE](./assets/phantom_os_logo.gif)  

---

## 📜 About

**PHANTOM-OS DATAGLOVE** is a **virtual plug-and-play driver system** designed for **RAG Developers**, initially supporting **webcam** or **file-based** gesture capture using **colored gloves** for motion plotting.  
The project integrates with **[LIONS MAPPER](https://github.com/ssmool/LIONSMAPPERAI)** for coordinate tracking and gesture mapping, enabling precise cursor and keyboard control from simple movie captures.  

> Made by developers, for developers — with the flexibility to extend and add support for multiple glove types in virtual driver mode.

This project is part of **CineOS Barsotti Unix-Like @BuskPlay**, currently **under construction** and coming soon with support for **RAG** and **Gen-AI** makers, targeted at **Officers, Studios, Desktop/Server environments, and Developers**.

---

## ⚙ Minimal Requirements

Install dependencies:

```bash
pip install tkinter keyboard pyautogui pillow lionsmapper
````

or

pip install tkinter keyboard pyautogui pillow lionsmapper

```bash
pip install phantomos
````


## 🖥 Screen & Device Configuration

### **Set Screen Source**

```python
set_ecran(ecran_src=0)  # Set the screen index (0 for primary)
```

### **Keyboard Mapping**

```python
set_keyboard(_axis)               # Assign key for press action
set_keyboard_return(_axis)        # Assign key for backspace/return
find_map_keyboard(_x, _y, _value) # Map virtual keys by x/y position, append char to list
```

### **Mouse Mapping**

```python
set_mouse({"x": 0, "y": 0}) # Move cursor pointer by axis
```

### **Open Virtual Interfaces**

```python
open_virtual_keyboard()  
# Opens a keyboard window using keyboard.png layout

open_virtual_mouse(
    RGB_DATAGLOVE_LEFT, RGB_DATAGLOVE_RIGHT, RGB_LEFT_CLICK,
    RGB_RIGHT_CLICK, RGB_SCROLL_DOWN, RGB_SCROLL_UP, RGB_CURSOR
)
# Assign gesture-to-mouse driver mappings
```

---

## 🧤 Data Glove Configuration

Edit **`data_glover.py`** to set your glove side and finger color mappings.

```python
set_dataglove_side("LEFT")  # Options: "LEFT" or "RIGHT"

LEFT_GLOVE = {
    "FINGER_1": "0,0,0",
    "FINGER_2": "0,0,0",
    "FINGER_3": "0,0,0",
    "FINGER_4": "0,0,0",
    "FINGER_5": "0,0,0"
}
```

### Retrieve Configurations

```python
get_dataglove()         # Returns dataglove color/position configuration
get_dataglove_cursor()  # Returns cursor mapping configuration
```

---

## 🚀 Starting the DataGlove

```python
start_dataglove()  # Starts webcam-based gesture detection (after configuration)
```

---

## 📚 Examples

**Example: Left Glove Cursor Control**

```python
set_ecran(0)
set_mouse({"x": 100, "y": 200})
open_virtual_mouse(
    RGB_DATAGLOVE_LEFT="255,0,0",
    RGB_DATAGLOVE_RIGHT="0,255,0",
    RGB_LEFT_CLICK="0,0,255",
    RGB_RIGHT_CLICK="255,255,0",
    RGB_SCROLL_DOWN="128,128,128",
    RGB_SCROLL_UP="64,64,64",
    RGB_CURSOR="0,255,255"
)
start_dataglove()
```

---

## 📖 Complete Manual

📄 **Full Documentation:** [PHANTOM-OS DATAGLOVE Manual for RAG Developers](./manual/manual_phantom_os_dataglove.MD)

---

## 💬 Comments

This project is part of **CineOS Barsotti Unix-Like** under **@BuskPlay**, in **pre-release** stage.
We are building this with **RAG** + **Gen-AI** support for **Officers, Studios, Desktop, Servers, and Developers**.

Contact: **@asytrick**
📧 **[eusmool@gmail.com](mailto:eusmool@gmail.com)**
🔗 **[https://github.com/ssmool](https://github.com/ssmool)**

---

