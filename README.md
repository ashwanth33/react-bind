import React, { useState } from "react";

const YourComponent = () => {
  const [obj, setObj] = useState({ amount_: 100, user_: "abc" });
  const handleAmountChange = (event) => {
    let value;
    if (!event.target.value) {
      value = 0;
      setObj({ ...obj, amount_: 0 });
    } else {
      value = parseInt(event.target.value);
      setObj({ ...obj, amount_: parseInt(event.target.value) });
    }

    console.log("amount_: " + value );
  };
  return (
    <div>
      <input type="text" value={obj.amount_} onChange={handleAmountChange} />
    </div>
  );
};

export default YourComponent;
