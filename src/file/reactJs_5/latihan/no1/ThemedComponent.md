import React, { useContext } from 'react';
import { ThemeContext } from './ThemeContext';

function ThemedComponent() {
  const { theme } = useContext(ThemeContext);

  const styles = {
    backgroundColor: theme === 'light' ? '#fff' : '#333',
    color: theme === 'light' ? '#000' : '#fff',
    padding: '20px',
    textAlign: 'center',
  };

  return (
    <div style={styles}>
      <h1>{theme === 'light' ? 'Light Theme' : 'Dark Theme'}</h1>
      <p>This is a {theme === 'light' ? 'bright and cheerful' : 'cool and dark'} theme!</p>
    </div>
  );
}

export default ThemedComponent;
