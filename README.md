# YourHealthMentor
<div class="review-container">
    <h2>Оставьте отзыв</h2>
    <form id="reviewForm">
        <textarea id="reviewText" placeholder="Напишите ваш отзыв..." rows="4" required></textarea>
        <button type="submit">Отправить</button>
    </form>
</div>

<div class="reviews">
    <h3>Отзывы:</h3>
    <div id="reviewsList"></div>
</div>

<script>
    // Простой код для добавления отзыва
    document.getElementById('reviewForm').addEventListener('submit', function(event) {
        event.preventDefault();
        const reviewText = document.getElementById('reviewText').value;

        if (reviewText) {
            const reviewElement = document.createElement('div');
            reviewElement.classList.add('review');
            reviewElement.textContent = reviewText;

            document.getElementById('reviewsList').appendChild(reviewElement);
            document.getElementById('reviewText').value = '';
        }
    });
</script>
<div class="chat-container">
    <h2>Чат</h2>
    <div id="chatBox"></div>
    <form id="chatForm">
        <input type="text" id="chatMessage" placeholder="Введите сообщение..." required />
        <button type="submit">Отправить</button>
    </form>
</div>

<script>
    // Простой код чата
    document.getElementById('chatForm').addEventListener('submit', function(event) {
        event.preventDefault();
        const message = document.getElementById('chatMessage').value;

        if (message) {
            const messageElement = document.createElement('div');
            messageElement.classList.add('chat-message');
            messageElement.textContent = message;

            document.getElementById('chatBox').appendChild(messageElement);
            document.getElementById('chatMessage').value = '';
        }
    });
</script>
