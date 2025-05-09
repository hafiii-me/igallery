# Ex.08 Design of Interactive Image Gallery
## Date : 09-05-2025
# NAME : MOHAMED HAFEEZ S
# REG NO : 212224040193

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
const images = [
  "https://picsum.photos/id/1015/600/400",
  "https://picsum.photos/id/1016/600/400",
  "https://picsum.photos/id/1018/600/400",
  "https://picsum.photos/id/1020/600/400",
  "https://picsum.photos/id/1024/600/400"
];

const gallery = document.getElementById("gallery");
const modal = document.getElementById("modal");
const modalImage = document.getElementById("modalImage");
const closeBtn = document.getElementById("close");
const nextBtn = document.getElementById("nextBtn");
const prevBtn = document.getElementById("prevBtn");

let currentIndex = 0;

// Load images into the gallery
images.forEach((src, index) => {
  const img = document.createElement("img");
  img.src = src;
  img.alt = `Image ${index + 1}`;
  img.addEventListener("click", () => openModal(index));
  gallery.appendChild(img);
});

function openModal(index) {
  currentIndex = index;
  modal.style.display = "flex";
  modalImage.src = images[currentIndex];
}

function closeModal() {
  modal.style.display = "none";
}

function nextImage() {
  currentIndex = (currentIndex + 1) % images.length;
  modalImage.src = images[currentIndex];
}

function prevImage() {
  currentIndex = (currentIndex - 1 + images.length) % images.length;
  modalImage.src = images[currentIndex];
}

// Event listeners
closeBtn.addEventListener("click", closeModal);
nextBtn.addEventListener("click", nextImage);
prevBtn.addEventListener("click", prevImage);

// Optional: close modal on outside click
modal.addEventListener("click", (e) => {
  if (e.target === modal) closeModal();
});

## OUTPUT:
![Screenshot 2025-05-09 142134](https://github.com/user-attachments/assets/465b88ef-7dda-416e-a8d9-383b2427d660)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
