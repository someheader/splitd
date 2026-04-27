# Design System: PartNest B (Refined)

## Overview
O PartNest B é um sistema de controle local para assinaturas compartilhadas. O design foca em simplicidade, legibilidade e uma estética premium que transmite segurança e organização, utilizando profundidade e contraste aprimorados.

## Visual Identity
O sistema suporta os modos **Dark** (Principal) e **Light** (Alternativo), utilizando roxo vibrante como cor de destaque.

### Colors (Dark Mode - Refined)
- **Background:** `#0C0C14` (Deep Navy/Black)
- **Surface:** `#161624` with 80% opacity and backdrop-blur (Glassmorphism)
- **Primary:** `#7C5DFA` (Vibrant Purple)
- **Secondary Primary:** `#9277FF` (Light Purple)
- **Text Primary:** `#FFFFFF`
- **Text Secondary:** `#DFE3FA` (Soft Blue/Grey)
- **Success:** `#33D69F`
- **Pending/Warning:** `#FF8F00`
- **Danger:** `#EC5757`

### Colors (Light Mode - Refined)
- **Background:** `#F8F9FF` (Off-white)
- **Surface:** `#FFFFFF` with multi-layered soft shadows
- **Primary:** `#7C5DFA`
- **Text Primary:** `#0C0E16`
- **Text Secondary:** `#7E88C3`
- **Border:** `#DFE3FA`

### Typography
- **Font Family:** 'Manrope', sans-serif.
- **Scale:**
  - **H1:** Bold, 32px, tracking tight.
  - **H2:** Bold, 24px.
  - **Body:** Regular/Medium, 14px-16px.
  - **Label:** Semibold, 12px, uppercase tracking wide.

## Components & Layout Patterns

### 1. Navigation (Desktop Rail)
- **Style:** Compact sidebar (64px).
- **Active State:** Primary color icon with a 10% opacity background pill of the same color.
- **Dark Mode:** Deep Navy background with subtle right border.
- **Light Mode:** White background with soft right border.

### 2. Cards
- **Style:** Border radius fixed at `20px`.
- **Depth (Dark):** Backdrop-blur (12px) and subtle 1px border (`white/10`).
- **Depth (Light):** Layered shadows: `box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.04), 0 8px 10px -6px rgba(0, 0, 0, 0.04)`.

### 3. Data Tables & Lists
- **Style:** Clean rows, no vertical borders.
- **Status Pills:** Bold text, high-contrast semantic backgrounds (15% opacity), and subtle matching borders.

### 4. Layout Grid
- **Desktop:** Compact rail + flexible content area.
- **Mobile:** Bottom navigation bar + single column layout.

## Design Principles
1.  **Glassmorphism & Depth:** Use blur and shadows to define hierarchy.
2.  **Strict Rounding:** Every card and button must use the 20px radius.
3.  **Action Contrast:** Primary actions (`#7C5DFA`) must always be the most prominent element.
4.  **Consistency:** Identical visual language across all screens and themes.