import React, { useContext } from 'react';
import { UserContext } from './UserContext';

function Login() {
  const { user, login, logout } = useContext(UserContext);

  const handleLogin = () => {
    const fakeUser = { name: 'John Doe', email: 'john@example.com' };
    login(fakeUser);
  };

  return (
    <div>
      {user ? (
        <button onClick={logout}>Logout</button>
      ) : (
        <button onClick={handleLogin}>Login</button>
      )}
    </div>
  );
}

export default Login;
