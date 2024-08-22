import React from 'react';
import { UserProvider } from './UserContext';
import UserProfile from './UserProfile';
import Login from './Login';

function App() {
  return (
    <UserProvider>
      <div>
        <h1>User Management with Context API</h1>
        <Login />
        <UserProfile />
      </div>
    </UserProvider>
  );
}

export default App;

