const express = require('express');
const app = express();
const port = 5000;

let tasks = []; 

app.use(express.json());

app.get('/tasks', (req, res) => res.json(tasks));
app.post('/tasks', (req, res) => {
  const task = req.body;
  tasks.push(task);
  res.status(201).json(task);
});
app.delete('/tasks/:id', (req, res) => {
  const { id } = req.params;
  tasks = tasks.filter(task => task.id !== id);
  res.status(204).send();
});

app.listen(port, () => console.log(`Backend running on port ${port}`));
 
