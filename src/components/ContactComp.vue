<template>
  <div>
    <div class="container-fluid">
      <center>
        <h1 class="h-01 text-white"><b>Contact Form</b></h1>
        <br>
      </center>
      <div class="form row">
        <div class="col-6 text-white colbrd">
          <br />
          <br />
          <b>
            <p class="fs-4 pad">ethanliamoliver28@gmail.com</p>
            <br />
            <br />
            <p class="fs-4 pad">Tel No: 021 555 8888</p>
            <br />
            <br />
            <p class="fs-4 pad">9010 Ackerman Ave, 5430</p>
            <br />
            <br />
            <p class="fs-4 pad">xxxx xxxx xxxx</p>
          </b>
        </div>
        <div class="col-6 text-white">
          <br />
          <br />
          <form action="https://formspree.io/f/{form_id}" method="post">
            <label for="First Name" class="fs-5">First Name</label>
            <br />
            <input type="text" class="input" placeholder="Enter First Name" />
            <br />
            <label for="Last Name" class="fs-5">Last Name</label>
            <br />
            <input type="text" class="input" placeholder="Enter Last Name" />
            <br />
            <label for="email" class="fs-5">Email Account</label>
            <br />
            <input
              name="Email"
              id="email"
              type="email"
              class="input"
              placeholder="example@gmail.com"
            />
            <br />
            <label for="" class="fs-5">Leave Us a Message</label>
            <br />
            <input type="text" class="inputmess" />
            <br />
            <br />
            <button type="submit">
              <span class="box text-white"> Send! </span>
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.pad {
  cursor: pointer;
}

.pad:hover {
  transform: scale(1.05);
  transition: ease-in 0.5s;
}

.colbrd {
    border-right: white solid;
}

.input {
  border-radius: 1.5rem;
  width: 16rem;
  height: 2.8rem;
}

input:hover {
    box-shadow: #ffffff 0px 0px 8px 8px;
    cursor: pointer;
}

.inputmess {
  border-radius: 1.5rem;
  height: 5.8rem;
  width: 16rem;
}

.box {
  width: 140px;
  height: auto;
  float: left;
  transition: .5s linear;
  position: relative;
  display: block;
  overflow: hidden;
  padding: 15px;
  text-align: center;
  margin: 0 5px;
  background: transparent;
  text-transform: uppercase;
  font-weight: 900;
}

.box:before {
  position: absolute;
  content: '';
  left: 0;
  bottom: 0;
  height: 4px;
  width: 100%;
  border-bottom: 4px solid transparent;
  border-left: 4px solid transparent;
  box-sizing: border-box;
  transform: translateX(100%);
}

.box:after {
  position: absolute;
  content: '';
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  border-top: 4px solid transparent;
  border-right: 4px solid transparent;
  box-sizing: border-box;
  transform: translateX(-100%);
}

.box:hover {
  box-shadow: 0 5px 25px rgb(23, 0, 128);
}

.box:hover:before {
  border-color: #00eaff;
  height: 100%;
  transform: translateX(0);
  transition: .3s transform linear, .3s height linear .3s;
}

.box:hover:after {
  border-color: #ffffff;
  height: 100%;
  transform: translateX(0);
  transition: .3s transform linear, .3s height linear .5s;
}

button {
  color: black;
  text-decoration: none;
  cursor: pointer;
  outline: none;
  border: none;
  background: transparent;
}
</style>
