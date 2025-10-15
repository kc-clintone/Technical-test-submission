# Front-end, React Example

## Q3:

I will use React.js for this problem, here is my solution:

```
import React, { useEffect, useState } from 'react';

function Profile() {
  // To help manage data states
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(false);

  useEffect(() => {
    // fetch the user inside a use effect
    fetch('https://jsonplaceholder.typicode.com/users/1')
      .then(res => res.json())
      .then(data => {
        setUser(data);
        setLoading(false);
      })
      .catch(() => setError(true));
  }, []);

  // this is my little loading state and error state
  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error loading data.</p>;

  return (
    // then i return and render the fetched data inside a jsx component
    <div>
      <h1>{user.name}</h1>
      <p>{user.email}</p>
    </div>
  );
}
```


# Back-end / Logic:

## Q4: 

I will use python for this one:

```
def calculate_total(sales):
    return sum(item["price"] * item["quantity"] for item in sales)
```

### My explanation:
To calculate total revenue, I multiply price and quantity for each item, then I sum them up.
