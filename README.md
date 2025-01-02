# YourHealthMentor
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="">
    <meta name="author" content="">
    <meta name="csrf" content="" id="csrf">
    <link rel="shortcut icon" href="/img/tildafavicon.ico">
    <link rel="icon" href="/img/tildafavicon.svg" type="image/svg+xml">
    <link rel="apple-touch-icon" href="/img/tildafavicon-180x180.png" type="image/png">

    <title>Tilda - Reviews & Chat</title>

    <!-- Existing scripts and styles -->
    <script src="/js/jquery-1.10.2.min.js" type="text/javascript" onerror="this.loaderr='y';"></script>
    <link href="/front/css/t-normalize.min.css?v=9471" rel="stylesheet" onerror="this.loaderr='y';">
    <link href="/front/css/t-common.min.css?v=9471" rel="stylesheet" onerror="this.loaderr='y';">
    <link href="/front/css/t-page-all.min.css?v=9471" rel="stylesheet" onerror="this.loaderr='y';">
    <script type="text/javascript" src="/front/js/t-common.min.js?v=9471" onerror="this.loaderr='y';"></script>

    <!-- Chat and Review Styles -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <link href="/front/css/reviews-chat.css" rel="stylesheet" type="text/css">

    <!-- Custom JavaScript for Reviews and Chat -->
    <script src="/front/js/reviews-chat.js" type="text/javascript"></script>

</head>

<body style="margin:0px;" data-lang="" data-country="">

<!-- Fixed main menu -->
<div class="tp-menu" role="navigation" id="mainmenu">
    <div id="info-alert" style="position:fixed; width:100%; z-index:10000;"></div>
    <div class="tp-menu__wrapper"></div>
</div>
<!--/// Fixed main menu -->

<!-- Reviews Section -->
<div class="reviews-section" id="reviews-section">
    <h2>Leave a Review</h2>
    <form id="review-form" method="POST">
        <textarea id="review-text" name="review-text" placeholder="Write your review..." required></textarea>
        <button type="submit" class="submit-btn">Submit Review</button>
    </form>

    <h3>Recent Reviews:</h3>
    <div id="reviews-list">
        <!-- Reviews will be dynamically added here -->
    </div>
</div>

<!-- Chat Section -->
<div class="chat-section" id="chat-section">
    <h2>Chat with Users</h2>
    <div id="chat-messages">
        <!-- Chat messages will appear here -->
    </div>

    <textarea id="chat-input" placeholder="Type a message..." required></textarea>
    <button id="send-chat" class="submit-btn">Send</button>
</div>

<!-- Modal for Admin Chat Access (optional) -->
<div class="modal fade tm-popup tm-popup_fade" id="adminChatModal" tabindex="-1" role="dialog" aria-labelledby="adminChatModalLabel" aria-hidden="true">
    <div class="modal-dialog tm-popup__wrap">
        <div class="modal-content tm-popup__window" id="adminChatContent">
            <!-- Admin chat content will be loaded dynamically -->
        </div>
    </div>
</div>

<script type="text/javascript">
    // Handle Review Form Submission
    document.getElementById('review-form').addEventListener('submit', function(event) {
        event.preventDefault();
        var reviewText = document.getElementById('review-text').value;
        
        // Simulate review submission (replace with real API call)
        var reviewItem = document.createElement('div');
        reviewItem.classList.add('review-item');
        reviewItem.innerHTML = `<p>${reviewText}</p>`;
        document.getElementById('reviews-list').appendChild(reviewItem);
        
        // Clear input field
        document.getElementById('review-text').value = '';
    });

    // Handle Chat Message Send
    document.getElementById('send-chat').addEventListener('click', function() {
        var chatMessage = document.getElementById('chat-input').value;

        // Simulate sending chat message (replace with real API call)
        var chatItem = document.createElement('div');
        chatItem.classList.add('chat-message');
        chatItem.innerHTML = `<p>${chatMessage}</p>`;
        document.getElementById('chat-messages').appendChild(chatItem);

        // Scroll to the bottom of chat
        document.getElementById('chat-messages').scrollTop = document.getElementById('chat-messages').scrollHeight;

        // Clear input field
        document.getElementById('chat-input').value = '';
    });
</script>

<!-- Footer or Additional Content -->

</body>
</html>
