import React, { createContext, useState } from 'react';

// Membuat ThemeContext
export const ThemeContext = createContext();

// Membuat Provider untuk membungkus komponen
export const ThemeProvider = ({ children }) => {
  const [theme, setTheme] = useState('light'); // Tema default adalah 'light'

  // Fungsi untuk toggle antara light dan dark theme
  const toggleTheme = () => {
    setTheme((prevTheme) => (prevTheme === 'light' ? 'dark' : 'light'));
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};
