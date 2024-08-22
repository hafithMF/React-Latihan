import React, { createContext, useState } from 'react';

// Membuat UserContext
export const UserContext = createContext();

// Membuat Provider untuk membungkus komponen
export const UserProvider = ({ children }) => {
  const [user, setUser] = useState(null);

  // Fungsi untuk login pengguna
  const login = (userInfo) => {
    setUser(userInfo);
  };

  // Fungsi untuk logout pengguna
  const logout = () => {
    setUser(null);
  };

  return (
    <UserContext.Provider value={{ user, login, logout }}>
      {children}
    </UserContext.Provider>
  );
};
