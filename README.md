### Radio-Form-handle-and-validation-checkbox-React-Example

import React, { useState, useEffect } from “react”;
const Formfile = () => {
const [all1, setall1] = useState({
fname: “”,
check :false
})
const chng =(e)=>{
const newall1 = {…all1}
if(e.target.name === “check”){
newall1[e.target.name] = e.target.checked
setall1(newall1)
}else{
newall1[e.target.name] = e.target.value
setall1(newall1)
}
}
const submitform =(e)=>{
e.preventDefault()
console.log(all1)
}
return (
<div>
<div className=”mx-5 my-5 px-5">
<br />
<h5>Form Data</h5>
<br />
<form onSubmit={submitform}>
<label for=”fname”>First name:</label>
<br />
<input onBlur={chng} required type=”text” id=”fname” name=”fname” />
<br />
<br />
<input onBlur={chng} type=”checkbox” name=”check” />
<label for=”lname”>submit:</label>
<br />
<input type=”submit” value=”Submit” />
</form>
</div>
</div>
);
};
export default Formfile;
