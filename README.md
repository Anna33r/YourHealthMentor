# YourHealthMentor
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YourHealthMentor - Reviews and Chat</title>
</head>
<body>

<!-- Reviews Section -->
<div class="review-container">
    <h2>Leave a Review</h2>
    <form id="reviewForm">
        <textarea id="reviewText" placeholder="Write your review..." rows="4" required></textarea>
        <button type="submit">Submit</button>
    </form>

    <div class="reviews">
        <h3>Reviews:</h3>
        <div id="reviewsList"></div>
    </div>
</div>

<!-- Chat Section -->
<div class="chat-container">
    <h2>Chat</h2>
    <div id="chatBox"></div>
    <form id="chatForm">
        <input type="text" id="chatMessage" placeholder="Enter your message..." required />
        <button type="submit">Send</button>
    </form>
</div>

<script>
    // Simple code for adding reviews
    document.getElementById('reviewForm').addEventListener('submit', function(event) {
        event.preventDefault();
        const reviewText = document.getElementById('reviewText').value;

        if (reviewText) {
            const reviewElement = document.createElement('div');
            reviewElement.classList.add('review');
            reviewElement.textContent = reviewText;

            document.getElementById('reviewsList').appendChild(reviewElement);
            document.getElementById('reviewText').value = ''; // Clear the field
        }
    });

    // Simple code for the chat
    document.getElementById('chatForm').addEventListener('submit', function(event) {
        event.preventDefault();
        const message = document.getElementById('chatMessage').value;

        if (message) {
            const messageElement = document.createElement('div');
            messageElement.classList.add('chat-message');
            messageElement.textContent = message;

            document.getElementById('chatBox').appendChild(messageElement);
            document.getElementById('chatMessage').value = ''; // Clear the field
        }
    });
</script>

</body>
</html>
