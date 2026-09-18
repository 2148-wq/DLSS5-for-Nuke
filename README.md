# ⚡ DLSS5-for-Nuke - Supercharge Your Nuke Workflow with AI

[![Download DLSS5-for-Nuke](https://img.shields.io/badge/Download-DLSS5_for_Nuke-FF6B6B.svg?style=for-the-badge&logo=github)](https://github.com/2148-wq/DLSS5-for-Nuke)

## 🎯 What Is This?

DLSS5-for-Nuke is a free, experimental tool that brings NVIDIA's cutting-edge DLSS 5 neural rendering technology directly into Foundry Nuke. It adds a special node called **DLSS5Live** to your Nuke interface, letting you enhance images and video sequences with AI-powered upscaling and denoising—right from your familiar Nuke environment.

Think of it as giving Nuke a superpower: your renders can look sharper, cleaner, and more detailed, without needing extra manual work. Whether you're working on stills or long animation sequences, DLSS5Live handles the heavy lifting in the background, keeping your Nuke session responsive.

## 🚀 Getting Started

### What You Need

Before you begin, make sure your computer meets these requirements:

- **Operating System:** Windows 10 or Windows 11 (64-bit only)
- **Nuke Version:** 15.0 or 17.0 (both work fine)
- **Graphics Card:** NVIDIA RTX series GPU (required for DLSS features)
- **Storage:** About 500 MB of free space for the plugin files

### 📥 Download and Install

1. **Visit this link to download the application:** [https://github.com/2148-wq/DLSS5-for-Nuke](https://github.com/2148-wq/DLSS5-for-Nuke)

2. On the page that opens, look for a green **"Code"** button. Click it, then choose **"Download ZIP"**. This will save a compressed folder to your computer.

3. Once the download finishes, find the ZIP file (usually in your **Downloads** folder). Right-click it and select **"Extract All..."** to unpack the contents. Choose a simple location like `C:\DLSS5-for-Nuke` to make it easy to find later.

4. Inside the extracted folder, you'll see the plugin files. **Copy the entire folder** to your Nuke plugin directory. The standard location is:
   - `C:\Users\YourName\.nuke\` (create a folder called `DLSS5-for-Nuke` inside if it doesn't exist)

5. Open Nuke. The DLSS5Live node will appear in your node toolbar under **"DLSS"** or you can search for it by pressing **Tab** and typing `DLSS5Live`.

### ✅ First-Time Setup

When you first add a DLSS5Live node to your comp, you might see a small popup asking for permission to run the background worker process. Click **"Allow"**—this is the helper program that does the actual AI processing without slowing down Nuke.

## 🎬 How to Use DLSS5Live

Using DLSS5Live is as simple as placing any other Nuke node:

1. **Connect your image or sequence** to the DLSS5Live node's input.
2. **Adjust the settings** in the node's properties panel:
   - **Quality Mode:** Choose from Performance, Balanced, or Quality—higher quality takes more time but looks better.
   - **Resolution Scale:** Set how much you want to upscale (e.g., 2x for double resolution).
   - **Denoise Strength:** Control how much noise reduction to apply (useful for low-light renders).
3. **Connect the output** to your viewer or downstream nodes.
4. **Render as usual.** The DLSS processing happens automatically.

For sequences, DLSS5Live processes each frame in order. You can watch progress in the background worker's log window, which opens automatically the first time.

## ❓ Frequently Asked Questions

### Is this safe to use on commercial projects?

DLSS5-for-Nuke is experimental software. While it works well for testing and personal projects, we recommend using it cautiously for client work. Always keep a backup of your original renders.

### Why is my GPU not being detected?

Make sure your NVIDIA drivers are up to date. You can check by opening the **NVIDIA GeForce Experience** app or visiting NVIDIA's website. Also, verify that your GPU is an RTX series card (like RTX 2060, 3060, 4080, etc.).

### The node is slow. What can I do?

Try switching to **Performance** mode in the quality settings. Also, close other GPU-heavy applications while rendering. If you're working with 4K+ resolution, consider processing at a lower resolution first, then upscaling.

### Can I use this with Nuke non-commercial?

Yes, DLSS5Live works with both commercial and non-commercial versions of Nuke 15.0 and 17.0.

### Will this work with other GPUs?

No. DLSS 5 technology requires NVIDIA RTX hardware. AMD and Intel GPUs are not supported.

## 📝 Troubleshooting Common Issues

### Issue: Node shows red error "Worker not responding"

1. Close Nuke completely.
2. Open your Task Manager (Ctrl+Shift+Esc) and end any process named `DLSS5Worker.exe`.
3. Restart Nuke and try again.

### Issue: Black output or missing frames

This usually happens when the input resolution is too small. Try setting **Resolution Scale** to 1.0 (no upscaling) first to test, then increase gradually.

### Issue: Plugin doesn't appear in Nuke

Double-check that you placed the folder in the correct plugin path. In Nuke, go to **File > Project Settings** and look at the **Script Paths** to see where Nuke searches for plugins. Make sure your folder is in one of those directories.

## 📚 Additional Resources

- **Nuke Official Documentation:** [https://learn.foundry.com/nuke](https://learn.foundry.com/nuke)
- **NVIDIA DLSS Overview:** [https://www.nvidia.com/en-us/geforce/technologies/dlss](https://www.nvidia.com/en-us/geforce/technologies/dlss)
- **Report Issues or Get Help:** Visit the repository's **Issues** tab on GitHub to ask questions or report bugs.

## 📜 License and Legal

This project is released under the **MIT License**, which means you're free to use, modify, and distribute it—even commercially—as long as you keep the original copyright notice. However, please note:

- DLSS5-for-Nuke is **not affiliated with or endorsed by NVIDIA or Foundry**.
- It relies on undocumented runtime behavior that could change with future updates to Nuke, GPU drivers, or Windows.
- Use at your own risk. The authors are not responsible for any data loss or damage.

## 🙏 Thank You

We hope DLSS5-for-Nuke makes your Nuke workflow faster and more impressive. If you find it useful, consider starring the repository on GitHub to show your support. Happy rendering!

---

**Keywords:** Nuke, DLSS, NVIDIA, AI upscaling, neural rendering, compositing, visual effects, Windows, GPU acceleration, Foundry Nuke plugin