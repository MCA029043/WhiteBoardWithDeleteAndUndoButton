# Whiteboard Delete Undo Buttons

This repository contains a basic whiteboard application built using HTML, CSS, and JavaScript. The application provides users with the ability to draw on a canvas and includes buttons to delete the drawing and undo the last action.

## How it Works

- **HTML Structure**: The HTML structure consists of a canvas element for drawing, two buttons for delete and undo actions, and a container for the buttons.

- **CSS Styling**: The CSS code provides basic styling for the layout. It ensures that the canvas and buttons are properly positioned and styled.

- **JavaScript Logic**: The JavaScript code handles the drawing functionality, delete action, and undo action.

    - **Drawing**: The drawing functionality is initiated when the user clicks and holds the mouse button on the canvas. The `mousedown`, `mousemove`, and `mouseup` events are used to track and draw the path of the cursor. The drawn path is stored in a temporary array (`tempPath`) until the user releases the mouse button.

    - **Delete Action**: The "Delete" button (`deleteButton`) triggers the `clearWhiteboard` function, which clears the canvas and removes all stored drawing objects.

    - **Undo Action**: The "Undo" button (`undoButton`) triggers the `handleUndo` function. This function removes the last drawing object from the `objects` array and redraws the canvas based on the remaining drawing objects.

    - **Redrawing Canvas**: The `redrawCanvas` function clears the canvas and redraws all stored drawing objects using the stored paths. It iterates through the `objects` array and recreates the drawn paths.

    - **Object Management**: The `addObjectToCanvas` function is responsible for adding a new drawing object to the `objects` array. This is called when the user releases the mouse button after drawing.

## Usage

1. Open the `index.html` file in a web browser.
2. You'll see a canvas with "Delete" and "Undo" buttons below it.
3. Click and hold the mouse on the canvas to draw.
4. Use the "Delete" button to clear the canvas.
5. Use the "Undo" button to undo the last drawing action.

## Note

This application provides a basic whiteboard experience and can be further enhanced with features like different colors, line thickness options, and more advanced undo/redo functionality.
