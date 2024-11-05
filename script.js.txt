document.addEventListener('DOMContentLoaded', function () {
    const images = document.querySelectorAll('.carousel-image');
    let currentImageIndex = 0;

    function showNextImage() {
        images[currentImageIndex].classList.remove('active');
        currentImageIndex = (currentImageIndex + 1) % images.length;
        images[currentImageIndex].classList.add('active');
    }

    setInterval(showNextImage, 5000); // Muda a cada 5 segundos

    function updateTimeTogether() {
        const startDate = new Date('2022-08-11'); // Substitua pela data de início do relacionamento
        const now = new Date();
        const diff = now - startDate;

        const days = Math.floor(diff / (1000 * 60 * 60 * 24));
        const years = Math.floor(days / 365);
        const displayYears = ${years} anos;

        document.getElementById('timeTogether').innerText = displayYears;
    }

    updateTimeTogether();
});
