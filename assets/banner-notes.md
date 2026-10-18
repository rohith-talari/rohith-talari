# Custom banner implementation notes

The supplied Master Prompt calls for `dark.svg` and `light.svg` with a photo-derived dithered portrait, an animated logo morph, and a terminal-style information panel.

## Personal data for the banner

- Name: Talari Rohith
- GitHub handle: `rohith-talari`
- Role: B.Tech CSE (AI & ML) student / aspiring AI/ML engineer
- Origin: Hyderabad, India
- Education: SRM Institute of Science and Technology, Tiruchirappalli
- Status: Building · Learning · Shipping
- Toolchain: VS Code, Git, GitHub, Jupyter, Google Colab, PyCharm
- Core languages: Python, C, C++, Java (basics), MATLAB (basics)
- LinkedIn: `linkedin.com/in/rohith-talari`
- Email: `talarirohith001@gmail.com`

## Style from the PDF

- Canvas: 1180 × 610
- Terminal title: `profile.sh --live`
- Left ~38%: head-and-shoulders portrait, label `VISUAL.MAP`
- Right: `SYSTEM.INFO` readout, dotted leaders, LIVE indicator, handle pill
- Palette: `#0A101F` background, `#22D3EE` cyan, `#A78BFA` violet, `#10B981` green
- Create both dark and light assets and test in a browser.
- The photo should have a plain background, clear subject separation, even lighting, and sharp head-and-shoulders framing.
- Do not use a tight face crop or a busy background.

The photo-specific animation is not included because no portrait image was attached. Keep the source generator and any intermediate data with the SVGs so the design remains reproducible.
