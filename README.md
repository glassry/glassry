<!-- Add this HTML code in your website or README.md file -->
<p>My GitHub repositories: <span id="repoCount"></span></p>
<p>Visitors: <img src="https://visitor-badge.glitch.me/badge?page_id=Glassry.Teba" alt="Visitor Count"></p>

<!-- Add this JavaScript code at the end of the body section or just before the closing </body> tag -->
<script>
// Fetch the number of repositories from GitHub API
fetch('https://api.github.com/users/glassry/repos')
  .then(response => response.json())
  .then(data => {
    document.getElementById('repoCount').textContent = data.length;
  })
  .catch(error => console.error(error));
</script>
