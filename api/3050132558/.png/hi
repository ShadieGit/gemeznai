module.exports = async (req, res) => {
    const directGifUrl = 'https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdW8xaWJ3bnh6ZzF5bWZ5eGZ6ZzF5bWZ5eGZ6ZzF5bWZ5eGZ6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/aUXdLmZEiUXjS4LuCH/giphy.gif';
    try {
        const gifResponse = await fetch(directGifUrl);
        const gifBuffer = await gifResponse.arrayBuffer();
        res.setHeader('Content-Type', 'image/gif');
        res.setHeader('Cache-Control', 'public, max-age=3600');
        return res.status(200).send(Buffer.from(gifBuffer));
    } catch (error) {
        const base64Png = 'iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mNkYAAAAAYAAjCB0C8AAAAASUVORK5CYII=';
        res.setHeader('Content-Type', 'image/png');
        return res.status(200).send(Buffer.from(base64Png, 'base64'));
    }
};