# Q3: Front-end, React Example

I will use React.js for this problem, here is my solution:

```
import React, { useEffect, useState } from 'react';

function Profile() {
  // To help manage data states
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(false);

  useEffect(() => {
    fetch('https://jsonplaceholder.typicode.com/users/1')
      .then(res => res.json())
      .then(data => {
        setUser(data);
        setLoading(false);
      })
      .catch(() => setError(true));
  }, []);

  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error loading data.</p>;

  return (
    <div>
      <h1>{user.name}</h1>
      <p>{user.email}</p>
    </div>
  );
}
```


# Q4: Back-end / Logic:

I will use python for this one:

```
def calculate_total(sales):
    return sum(item["price"] * item["quantity"] for item in sales)
```

### My explanation:
First, I multiply price and quantity for each item, then I sum them up.
