document.getElementById('kv-form').addEventListener('submit', async (event) => {
    event.preventDefault();

    const formData = new FormData(event.target);
    const key = formData.get('key');
    const value = formData.get('value');

    try {
        const response = await fetch('https://worker-kvpost-demo.berta.workers.dev', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({ key, value }),
        });

        if (!response.ok) {
            throw new Error('Failed to store data');
        }

        const result = await response.text();
        document.getElementById('result').innerText = `Data stored successfully: ${result}`;
    } catch (error) {
        document.getElementById('result').innerText = `Error: ${error.message}`;
    }
});
