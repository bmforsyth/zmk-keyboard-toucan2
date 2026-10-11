# ZMK Firmware Coding Rules

1. **Strict ZMK Syntax:** This project uses ZMK firmware, not QMK. Never use QMK keycodes (e.g., `KC_A`, `MO(1)`) or macros. Strictly use ZMK behaviors (e.g., `&kp A`, `&mo 1`, `&bt BT_SEL 0`).
2. **Preserve Keymap Alignment:** When editing `.keymap` files, maintain the exact visual spacing and grid alignment of the existing bindings for readability. Do not auto-format, wrap lines, or collapse whitespace inside the `bindings = <...>` nodes.
3. **Devicetree Compliance:** Ensure all `.keymap` and `.overlay` files adhere to Zephyr Devicetree syntax. Do not delete existing `#include` directives or board/shield macro definitions.
4. **Kconfig Variables:** When editing `.conf` files, only use valid ZMK and Zephyr Kconfig flags (e.g., `CONFIG_ZMK_...=y` or `CONFIG_BT_...=y`). Do not invent configuration flags.
5. **Scoping:** Only modify files in the `config/` directory (like `config/toucan2.keymap` or `config/toucan2.conf`). Do not modify the underlying shield or board definition files unless explicitly instructed.
