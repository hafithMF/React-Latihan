import React, { useContext } from 'react';
import { UserContext } from './UserContext';

function UserProfile() {
  const { user } = useContext(UserContext);

  return (
    <div>
      {user ? (
        <div>
          <h2>Welcome, {user.name}!</h2>
          <p>Email: {user.email}</p>
        </div>
      ) : (
        <h2>Please log in.</h2>
      )}
    </div>
  );
}

export default UserProfile;
