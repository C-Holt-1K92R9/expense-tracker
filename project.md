Role: Senior Frontend Engineer & UI/UX Architect

Project Overview:
We are developing a lightweight, client-side financial tool named "Minimalist Single-Input Financial Ledger System." The core philosophy is to minimize user friction by eliminating complex forms, multi-step inputs, and visual clutter, allowing users to log expenses via a single natural-text input string in under 3 seconds.

Technical Specifications & Constraints:
1. Stack: Single-file architecture (HTML5, Tailwind CSS via CDN for rapid utility-first styling, and native Vanilla JavaScript/ES6+ for state management and DOM manipulation). No heavy frameworks or external bundlers.
2. Data Persistence: Implement client-side data persistence utilizing the Web Storage API (`localStorage`). All CRUD operations must directly synchronize with state and update the view without page reloads.
3. System Architecture:
   - Data Layer: An array of expense objects, each containing: `id` (timestamp-based uuid), `amount` (float), `description` (string), and `timestamp` (ISO string).
   - Core Logic (Parser Engine): Write a robust regular expression (Regex) parser that captures the data from a single input string. The parser must gracefully handle variable input orders:
     - Case A: "[Numeric Amount] [Text Description]" (e.g., "500 Food") -> Extract: Amount=500, Description="Food"
     - Case B: "[Text Description] [Numeric Amount]" (e.g., "Coffee 120") -> Extract: Amount=120, Description="Coffee"
   - Input Validation: Implement non-blocking, visual error handling if the input string lacks a valid numerical value or description.

UI/UX Architecture (High-Contrast Minimalist Aesthetic):
- Typographical Hierarchy: Use a clean, modern sans-serif font stack with ample white space and deliberate padding.
- Viewport Layout: Center-aligned, mobile-responsive card layout on a neutral, eye-pleasing background.
- Core Component 1 (Hero Metric): A prominent, high-visibility layout displaying the "Aggregate Monthly Expenditure" (dynamically formatted as a localized currency string).
- Core Component 2 (Smart Input): A single, auto-focused text field with high contrast and explicit focus states (`focus:ring-2`).
- Core Component 3 (Ledger View): A highly scannable datatable rendering recent transactions sorted chronologically (newest first). Include an asynchronous delete mechanism (action icon) per entry for instantaneous state removal.

Deliverables:
Provide a comprehensive, clean, and modular single-file HTML solution containing fully implemented structural layout, styling, and system logic. Avoid placeholder comments; ensure all edge-case parsing and storage interactions are fully executable.