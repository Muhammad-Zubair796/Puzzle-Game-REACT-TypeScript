

```markdown
# ⚛️ Assembly: The TypeScript Evolution

This is a complete refactor of my original [Puzzle-React-Game](https://github.com/Muhammad-Zubair796/Puzzule-React-Game). I took the same core logic and UI but rebuilt it using **TypeScript** to demonstrate how to build robust, type-safe React applications.



---

## 🛠️ The Challenge: From JS to TS

In the previous version, the app was prone to runtime errors because data (props) could be anything. In this version, I implemented a strict type system to ensure the app is "bulletproof."

### Key Upgrades in this Version:
* **Prop Interfaces:** Every component now has a defined `type` or `interface` for its props.
* **Generic State:** State hooks are now typed (e.g., `useState<string[]>`) so the compiler knows exactly what's inside our arrays.
* **Function Typing:** Callback functions like `addGuessedLetter` are strictly typed to prevent passing the wrong data back to the parent state.
* **Advanced Type Utilities:** Used `Omit` to pick specific properties from types for styling purposes.

---

## 📂 Component Breakdown (TypeScript Edition)

### 🔹 LanguageChips.tsx
Uses a `Language` type and the `Omit` utility to safely map through programming languages and apply dynamic styles.
```typescript
type Language = {
    name: string;
    backgroundColor: string;
    color: string;
}

```

### 🔹 WordLetters.tsx

Handles the secret word display. I typed the `.map()` parameters to ensure the `letter` and `index` are always a `string` and `number`.

### 🔹 Keyboard.tsx

The most complex part. It handles the logic for disabled states and user input using a typed function prop:

```typescript
addGuessedLetter: (letter: string) => void

```

---

## 🚀 Technical Features

* **Type Safety:** 100% TS coverage.
* **Accessibility:** Maintained `aria-live` and `aria-label` support for screen readers.
* **Conditional Styling:** Used the `clsx` library for clean, readable class management.
* **Logic Isolation:** Separated the "Farewell Messages" and language data into modular files.

---

## 🔧 How to Run

1. **Clone the Repo:**
```bash
git clone [https://github.com/Muhammad-Zubair796/Puzzle-Game-REACT-TypeScript.git](https://github.com/Muhammad-Zubair796/Puzzle-Game-REACT-TypeScript.git)

```


2. **Install Packages:**
```bash
npm install

```


3. **Start Local Server:**
```bash
npm run dev

```



---

## 👨‍💻 Reflection

Refactoring this game from JavaScript to TypeScript helped me understand how **Type-Driven Development** catches bugs during coding rather than after deployment. It makes the codebase much more maintainable and professional.

---

```

---

