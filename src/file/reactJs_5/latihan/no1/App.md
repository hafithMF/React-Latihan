import React from 'react';
import { ThemeProvider } from './ThemeContext';
import ThemeSwitcher from './ThemeSwitcher';
import ThemedComponent from './ThemedComponent';

function App() {
  return (
    <ThemeProvider>
      <div>
        <ThemeSwitcher />
        <ThemedComponent />
      </div>
    </ThemeProvider>
  );
}

export default App;
