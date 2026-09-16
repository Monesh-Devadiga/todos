# Todo
A single-page Todo built with React. Demonstrates component-based thinking and centralized state management.

## Features
- Add, toggle, edit (double-click) and delete tasks
- Filter by All / Active / Completed
- Clear completed in one click
- Live item counter
- Persists to `localStorage` (survives page reloads)
- Responsive, keyboard-friendly (Enter saves, Escape cancels editing)

## Project structure
```
src/
  App.jsx                 # Single source of truth for state + all handlers
  main.jsx                # React entry point
  index.css               # App styles
  components/
    TodoInput.jsx         # Add-task form (local form state only)
    TodoList.jsx          # Renders list or empty state
    TodoItem.jsx          # One task: toggle, inline edit, delete
    TodoFooter.jsx        # Filters, item count, clear completed
```
State lives in one place (`App.jsx`): the `todos` array and the active `filter`. Derived values (`filteredTodos`, `activeCount`) are computed there and passed down as props, so child components stay presentational.

## Getting started
```bash
npm install
npm run dev      # start dev server at http://localhost:5173
```

