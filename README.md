## Date:

## AIM
To create a Image Carousel using React 

## ALGORITHM
### STEP 1 Initial Setup:
Input: A list of images to display in the carousel.

Output: A component displaying the images with navigation controls (e.g., next/previous buttons).

### Step 2 State Management:
Use a state variable (currentIndex) to track the index of the current image displayed.

The carousel starts with the first image, so initialize currentIndex to 0.

### Step 3 Navigation Controls:
Next Image: When the "Next" button is clicked, increment currentIndex.

If currentIndex is at the end of the image list (last image), loop back to the first image using modulo:
currentIndex = (currentIndex + 1) % images.length;

Previous Image: When the "Previous" button is clicked, decrement currentIndex.

If currentIndex is at the beginning (first image), loop back to the last image:
currentIndex = (currentIndex - 1 + images.length) % images.length;

### Step 4 Displaying the Image:
The currentIndex determines which image is displayed.

Using the currentIndex, display the corresponding image from the images list.

### Step 5 Auto-Rotation:
Set an interval to automatically change the image after a set amount of time (e.g., 3 seconds).

Use setInterval to call the nextImage() function at regular intervals.

Clean up the interval when the component unmounts using clearInterval to prevent memory leaks.

## PROGRAM
App.jsx
```
import React from 'react';
import FoodDisplay from './components/FoodDisplay';

function App() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-orange-50 to-orange-100 flex items-center justify-center py-12">
      <FoodDisplay />
    </div>
  );
}

export default App;
```
App.css
```
@tailwind base;
@tailwind components;
@tailwind utilities;+
```

## OUTPUT
<img width="2558" height="1599" alt="444786604-0c1c7ed8-f436-47c3-8cd5-b2e2882fc81a" src="https://github.com/user-attachments/assets/9d846632-e1b2-416e-ac9b-d6536eba805d" />
<img width="2559" height="1599" alt="444786620-411570d3-aeb4-49ab-bdd7-399233b516da" src="https://github.com/user-attachments/assets/dfdf8c07-e81d-4c86-81bc-dea3e2648cf5" />
<img width="2559" height="1599" alt="444786630-65ac8942-b6e0-4155-acda-1745010210a0" src="https://github.com/user-attachments/assets/340bbf5e-c54c-4b0f-868c-1dea811be26c" />



## RESULT
The program for creating Image Carousel using React is executed successfully.
