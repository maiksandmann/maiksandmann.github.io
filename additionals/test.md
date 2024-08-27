<br>
<br>

<h2>Submit a GitHub Issue</h2>
<form id="issueForm">
    <label for="title">Title:</label><br>
    <input type="text" id="title" name="title" required><br><br>
    <label for="body">Description:</label><br>
    <textarea id="body" name="body" required></textarea><br><br>
    <button type="submit">Submit Issue</button>
</form>

<script>
    document.getElementById('issueForm').addEventListener('submit', async function(event) {
        event.preventDefault();
        const title = document.getElementById('title').value;
        const body = document.getElementById('body').value;
        const repo = 'maiksandmann/maiksandmann.github.io'; // Replace with your repository
        const token = 'Y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'; // Replace with your GitHub personal access token

        const response = await fetch(`https://api.github.com/repos/${repo}/issues`, {
            method: 'POST',
            headers: {
                'Authorization': `token ${token}`,
                'Accept': 'application/vnd.github.v3+json'
            },
            body: JSON.stringify({
                title: title,
                body: body
            })
        });

        if (response.ok) {
            alert('Issue submitted successfully!');
        } else {
            alert('Failed to submit issue.');
        }
    });
</script>


<br>
<br>
<br>


<nav>
    <ul>
        {% for item in site.data.menu %}
            <li>
                <a class="{% if page.url == item.link %}active{% endif %}" href="{{ item.link }}">{{item.title}}</a>
            </li>
        {% endfor %}
    </ul>
</nav>

<style>
    nav ul {
        display: flex;
        list-style: none;
    }
    nav ul li {
        margin-right: 10px;
    }
    nav ul li a {
        text-decoration: none;
    }
</style>

<h2>Submit a GitHub Issue</h2>
<form id="issueForm">
    <label for="title">Title:</label><br>
    <input type="text" id="title" name="title" required><br><br>
    <label for="body">Description:</label><br>
    <textarea id="body" name="body" required></textarea><br><br>
    <label for="labels">Labels (comma-separated):</label><br>
    <input type="text" id="labels" name="labels"><br><br>
    <button type="submit">Submit Issue</button>
</form>

<script>
    document.getElementById('issueForm').addEventListener('submit', async function(event) {
        event.preventDefault();
        const title = document.getElementById('title').value;
        const body = document.getElementById('body').value;
        const labels = document.getElementById('labels').value.split(',').map(label => label.trim());
        const repo = 'maiksandmann/maiksandmann.github.io'; // Replace with your repository
        const token = 'Y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'; // Replace with your GitHub personal access token

        const response = await fetch(`https://api.github.com/repos/${repo}/issues`, {
            method: 'POST',
            headers: {
                'Authorization': `token ${token}`,
                'Accept': 'application/vnd.github.v3+json',
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                title: title,
                body: body,
                labels: labels
            })
        });

        if (response.ok) {
            alert('Issue submitted successfully!');
        } else {
            alert('Failed to submit issue.');
        }
    });
</script>


<br>
<br>
<br>