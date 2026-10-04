# PrismPick-Wallpapers

The official wallpaper library for **PrismPick** and **PrismPane** by PixelFF.

This repository provides the default wallpaper collection used by PrismPick and hosts the built-in default wallpaper shipped with PrismPane.

---

## Related Projects

### [PrismPane](https://github.com/PixelFFHQ/PrismPane)

A wallpaper-first frosted glass Discord theme by PixelFF.

### [PrismPick](https://github.com/PixelFFHQ/PrismPick)

A Vencord plugin for browsing and applying Discord wallpapers from GitHub-hosted image libraries.

---

## Official Library

PrismPick uses this repository by default.

### GitHub API

```text
https://api.github.com/repos/PixelFFHQ/PrismPick-Wallpapers/contents/backgrounds
```

### Public Wallpaper URL

```text
https://pixelffhq.github.io/PrismPick-Wallpapers/backgrounds/
```

PrismPick reads the file list through the GitHub API and loads the actual wallpaper images through GitHub Pages.

---

## Repository Structure

```text
PrismPick-Wallpapers/
├── backgrounds/
│   ├── PrismPane-Default.png
│   ├── Wallpaper-One.jpg
│   ├── Wallpaper-Two.webp
│   └── ...
└── README.md
```

All wallpapers intended to appear in PrismPick should be placed directly inside:

```text
backgrounds/
```

PrismPick currently reads that folder directly and does not recursively scan wallpaper subfolders.

---

## PrismPane Default Wallpaper

The default wallpaper used by PrismPane is:

```text
PrismPane-Default.png
```

Direct URL:

```text
https://pixelffhq.github.io/PrismPick-Wallpapers/backgrounds/PrismPane-Default.png
```

PrismPane loads this wallpaper automatically when no PrismPick wallpaper override is active.

Selecting another wallpaper through PrismPick temporarily overrides the PrismPane default.

Using **Disable Background** in PrismPick removes that override and allows PrismPane's default wallpaper to appear again.

---

## Supported Image Formats

PrismPick currently recognizes:

```text
.png
.jpg
.jpeg
.webp
.gif
```

For most wallpapers, JPEG or WebP are recommended because they can provide good visual quality at smaller file sizes.

PNG works well for artwork where lossless quality is important.

Animated GIF wallpapers are supported, but may use more system resources.

---

## Recommended Wallpaper Sizes

### Standard / Landscape

Recommended:

```text
2560 × 1440
```

or:

```text
3840 × 2160
```

1920 × 1080 will also work, but higher-resolution images generally hold up better when Discord resizes or crops the wallpaper.

### Portrait

For portrait-oriented Discord layouts:

```text
1440 × 2560
```

Portrait versions can be stored in the same `backgrounds` folder using descriptive filenames such as:

```text
NeonGlass.jpg
NeonGlass-Portrait.jpg
```

---

## Designing Wallpapers for PrismPane

PrismPane uses translucent and frosted interface panels, so wallpapers work best when they provide visual interest without making text difficult to read.

Good PrismPane wallpapers generally have:

- darker or calmer areas behind common UI regions
- strong central composition
- limited fine detail near the outer edges
- good contrast between bright and dark areas
- cyan, blue, purple, and magenta tones that complement the PixelFF palette
- enough resolution to survive `background-size: cover` cropping

The wallpaper may be cropped differently depending on:

- Discord window size
- monitor aspect ratio
- portrait or landscape orientation
- sidebar widths
- member-list visibility

Keeping important subjects away from the extreme edges usually produces the best results.

---

# Creating Your Own PrismPick Wallpaper Library

PrismPick is not limited to the official PixelFF wallpaper collection.

You can create your own public GitHub repository and point PrismPick at it.

---

## 1. Create a GitHub Repository

Create a new **public** GitHub repository.

Example:

```text
My-PrismPick-Wallpapers
```

Adding a README is recommended.

A `.gitignore` is not normally necessary for a simple wallpaper repository.

---

## 2. Create a Backgrounds Folder

Create:

```text
backgrounds/
```

Place your wallpaper files directly inside it.

Example:

```text
My-PrismPick-Wallpapers/
├── backgrounds/
│   ├── Space.jpg
│   ├── Forest.png
│   ├── NeonCity.webp
│   └── Aurora-Portrait.jpg
└── README.md
```

---

## 3. Enable GitHub Pages

Open your repository and go to:

**Settings → Pages**

Under **Build and deployment**, select:

```text
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

Save the settings.

GitHub may take a short time to deploy the site.

---

## 4. Test a Wallpaper URL

If your GitHub username is:

```text
ExampleUser
```

and your repository is:

```text
My-PrismPick-Wallpapers
```

a wallpaper named:

```text
Space.jpg
```

should be available at:

```text
https://ExampleUser.github.io/My-PrismPick-Wallpapers/backgrounds/Space.jpg
```

Open the URL directly in a browser.

If the image loads, the GitHub Pages side of the library is working.

---

## 5. Configure PrismPick

Open PrismPick settings in Discord.

Set **Library API URL** to:

```text
https://api.github.com/repos/ExampleUser/My-PrismPick-Wallpapers/contents/backgrounds
```

Set **Library Base URL** to:

```text
https://ExampleUser.github.io/My-PrismPick-Wallpapers/backgrounds/
```

Then select:

**Refresh Backgrounds**

Your wallpapers should appear in the PrismPick gallery.

---

## File Naming Tips

Simple filenames are recommended.

Good:

```text
Aurora.jpg
Neon-City.png
Purple-Space.webp
Forest-Portrait.jpg
```

Try to avoid extremely long filenames or unusual characters.

PrismPick safely URL-encodes filenames, but simple names are easier to manage and share.

GitHub Pages paths are case-sensitive, so:

```text
PrismPane-Default.png
```

and:

```text
prismpane-default.png
```

are different paths.

---

## Adding New Wallpapers

To add wallpapers to a PrismPick library:

1. Upload the new image into `backgrounds/`.
2. Commit the change.
3. Wait for GitHub Pages to update if necessary.
4. Open PrismPick.
5. Select **Refresh Backgrounds**.

The new wallpaper should appear automatically.

No PrismPick code changes are required.

---

## Removing Wallpapers

Deleting a wallpaper from the repository removes it from the gallery after the next refresh.

If a deleted wallpaper is currently selected, PrismPick may still remember its old URL until another wallpaper is selected or the background is disabled.

---

## Performance Recommendations

For a smooth experience:

- avoid unnecessarily huge image files
- compress photographic wallpapers when possible
- prefer JPEG or WebP for large photographic images
- reserve PNG for artwork that benefits from lossless quality
- be cautious with very large animated GIFs

A good general target is approximately:

```text
1–5 MB per wallpaper
```

Smaller is better when visual quality remains acceptable.

---

## Wallpaper Usage

Only upload wallpapers that you created yourself or that you have permission to distribute.

Do not add copyrighted artwork, photography, characters, logos, or other material unless you have the appropriate rights to redistribute it.

Individual wallpaper usage terms may be documented separately where necessary.

---

## Wallpaper Rights

PrismPick-Wallpapers contains a mix of original and third-party wallpaper artwork.

All third-party artwork remains the property of its respective creator or rights holder.

If you are a rights holder and would like an image removed, please open an issue or contact PixelFF and it will be removed promptly.

---

## Branding

The PixelFF, PrismPick, and PrismPane names, logos, and associated branding are not granted for use as official branding for third-party wallpaper libraries.

Third-party libraries may state that they are **compatible with PrismPick**.

They must not represent themselves as official PixelFF wallpaper libraries unless explicitly authorized by PixelFF.

---

## About PixelFF

PrismPick-Wallpapers is maintained by **PixelFF**.

Built and curated by **Hush / PixelFF**.
