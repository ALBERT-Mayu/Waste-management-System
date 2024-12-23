// JavaScript for interactivity can be added here.
document.addEventListener('DOMContentLoaded', () => {
    // Example: Display a moving object effect
    const movingObject = document.createElement('div');
    movingObject.style.width = '50px';
    movingObject.style.height = '50px';
    movingObject.style.backgroundColor = 'red';
    movingObject.style.position = 'absolute';
    movingObject.style.top = '50px';
    movingObject.style.left = '0';
    document.body.appendChild(movingObject);

    let pos = 0;
    const id = setInterval(() => {
        if (pos >= window.innerWidth) {
            clearInterval(id);
            document.body.removeChild(movingObject); // Remove it when it reaches the end
        } else {
            pos++;
            movingObject.style.left = pos + 'px';
        }
    }, 5);
});
