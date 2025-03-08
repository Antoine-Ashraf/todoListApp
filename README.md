# Todo List Application

A dynamic packing list application built with React.js, leveraging modern component-based architecture and state management techniques.

## 🛠️ Technical Stack & Features

### React.js Core Concepts
- **Component Composition**: Structured into reusable components (App, Form, PackingList, Item, Stats) following single responsibility principle
- **State Management**: Utilizes React's `useState` hook for:
  - Form input control (controlled components)
  - List item manipulation (CRUD operations)
  - Sorting preferences management
- **Props Drilling**: Implements parent-child communication pattern for:
  - Item addition/deletion
  - Packing status toggling
  - List clearing functionality
- **List Rendering**: Efficient rendering with `Array.map()` and unique `key` prop assignment
- **Conditional Rendering**: Dynamic UI updates based on packing progress and empty states

### Advanced React Patterns
- **Derived State**: Computes sorted list versions without mutating original state:
  - Input order sorting (default)
  - Alphabetical sorting using `localeCompare()`
  - Packed status sorting with numerical conversion
- **Functional Updates**: Implements state updates using previous state in `setItems`
- **Immutable State Operations**: Uses `filter()`, `map()`, and `slice()` for state transformations

### Key Features Implementation
- **Dynamic Form Controls**:
  - Quantity selector generated programmatically with `Array.from({ length: 20 })`
  - Input validation with empty description prevention
- **Item Management**:
  - Auto-generated unique IDs using `Date.now()`
  - Line-through styling through inline conditional styling
  - Batch deletion confirmation dialog
- **Progress Tracking**:
  - Real-time stats calculation using `filter()` and `Math.round()`
  - Completion percentage with edge-case handling (100% packed state)

### Project Structure
- Modular component organization with separation of concerns
- React 18 rendering with `createRoot` API
- Strict Mode enabled for development checks
- CSS className-based styling system
