# Anti-AI Vibecoding & Production UI/UX Standards

When designing, generating, or refactoring web and mobile user interfaces, strictly enforce these human-crafted product design principles:

### 1. Iconography & Visual Cleanliness
- **Zero Decorative Emojis**: Never use native OS emojis (e.g., 🚀, 💡, 🔥, ⚡, 📦) as interface icons. Emojis make products feel like cheap AI prototypes.
- **Standard Vector Icons Only**: Always use crisp SVG interface icons (Lucide, Phosphor, Heroicons) with consistent stroke widths (1.5px to 2px).

### 2. The 4-Layer Color Architecture (No AI Neon Palettes)
Never allow arbitrary color picking. All UIs must adhere to a strict 4-layer stack:
1. **Layer 0 (Canvas)**: Deep neutral anchor (#070A0F, #0B0F17, or pure #FFFFFF).
2. **Layer 1 (Surfaces & Cards)**: Subtle contrast elevation (`bg-white/[0.03]` with `border-white/10` on dark mode; `bg-slate-50` with subtle border on light mode).
3. **Layer 2 (Nested Groupings & Inputs)**: Recessed containers (`bg-black/40` or `bg-slate-100`) to hold code, tables, or machine-readable fields.
4. **Layer 3 (Functional Accents & Semantics)**: 
   - Primary brand color strictly bounded to active states, focused inputs, and primary CTAs.
   - Semantic colors (Emerald for success, Rose for destructive/error, Amber for warnings) reserved purely for communicating status, never for general decoration.

### 3. Data-Driven Form & Numeric Alignment
- **Let Data Shape the Component**: 
  - Finite categories/statuses belong in compact chips/pills.
  - Numbers and currency metrics must always be **right-aligned** so digits line up by place value.
  - Time-delineated data belongs in timelines or micro-charts, not raw multi-column tables.
- **Proximity & Typographic Hierarchy**:
  - On dashboards, keep font sizes compact (11px to 14px) with tight line heights. Large display fonts belong only on landing hero banners.
  - Secondary metadata should use muted opacities (slate-400 at 55–70% opacity) rather than custom colors.

### 4. Progressive Disclosure & The Spectrum of Explicitness
- **Avoid Screen Vomit**: Never repeat the same 4 KPI blocks across multiple tabs or crowd primary screens with secondary controls.
- **Contextual Actions**: Keep rare actions (delete, export, filter) hidden until hovered or tucked into popovers/menus. Primary triggers remain visible.
- **Optimistic Micro-Interactions**: Provide instant tactile feedback on click/press (`active:scale-98` or instant state change) before waiting on server requests.

### 5. Mobile Ergonomics
- Maintain single-direction scroll per section (vertical stack OR horizontal card snap, never chaotic multi-axis).
- Interactive targets must always maintain minimum 44px hit-areas.
- Use floating bottom action bars (3 to 4 icons max) and bottom sheets instead of overflowing desktop sidebars.

