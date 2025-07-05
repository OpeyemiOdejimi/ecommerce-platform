# ecommerce-platform

```
import React, { useEffect, useState } from 'react';
import axios from 'axios';

function App() {
  const [products, setProducts] = useState([]);

  useEffect(() => {
    axios.get('http://localhost:5000/products').then(res => {
      setProducts(res.data);
    });
  }, []);

  return (
    <div>
      <h1>Products</h1>
      <ul>{products.map(p => <li key={p.id}>{p.name}</li>)}</ul>
    </div>
  );
}

export default App;

```
