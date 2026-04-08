# twitter-clone-
this is my game
<h2>Twitter Clone 🐦</h2>

<textarea id="tweetInput" placeholder="What's happening?"></textarea>
<br>
<button onclick="postTweet()">Tweet</button>

<div id="tweets"></div>

<script>
function postTweet() {
  let input = document.getElementById("tweetInput");
  let text = input.value;

  if (text === "") return;

  let div = document.createElement("div");
  div.innerHTML = text + " <button onclick='this.parentElement.remove()'>Delete</button>";

  document.getElementById("tweets").prepend(div);
  input.value = "";
}
</script>
