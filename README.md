import React from "react";
import PropTypes from "prop-types";

const Welcome = ({ name }) => {
  return <h2>Welcome, {name}!</h2>;
};

Welcome.propTypes = {
  name: PropTypes.string.isRequired
};

export default function App() {
  const students = ["Deepak", "Nitin", "Amit"];
  return (
    <div>
      {students.map((s) => (
        <Welcome key={s} name={s} />
      ))}
    </div>
  );
}

output is - 
Welcome, Deepak!
Welcome, Nitin!
Welcome, Amit!
