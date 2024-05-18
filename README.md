import React, { useState, useEffect } from 'react';
import './App.css';
import Quote from './Quote';

function App() {
  const [quote, setQuote] = useState('');

  useEffect(() => {
    fetchRandomQuote();
  }, []);

  const fetchRandomQuote = async () => {
    const response = await fetch('https://quote-garden.herokuapp.com/api/v3/quotes/random');
    const data = await response.json();
    setQuote(data.data[0].quoteText);
  };

  return (
    <div className="App">
      <header className="App-header">
        <h1>Random Quote Generator</h1>
        <Quote text={quote} />
        <button onClick={fetchRandomQuote}>New Quote</button>
      </header>
    </div>
  );
}

export default App;
