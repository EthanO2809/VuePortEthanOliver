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
            <p class="pad">ethanliamoliver28@gmail.com</p>
            <br />
            <br />
            <p class="pad">Tel No: 021 555 8888</p>
            <br />
            <br />
            <p class="pad">9010 Ackerman Ave, 5430</p>
            <br />
            <br />
            <p class="pad">xxxx xxxx xxxx</p>
          </b>
        </div>
        <div class="col-6 text-white">
          <br />
          <br />
          <form action="https://formspree.io/f/mgejeopn" method="post">
            <label for="First Name" class="fs-5">First Name</label>
            <br />
            <input type="text" class="input" placeholder="Enter First Name" name="name" required oninvalid="this.setCustomValidity('Please Enter Your Name')"
            oninput="this.setCustomValidity('')" />
            <br />
            <label for="Last Name" class="fs-5">Last Name</label>
            <br />
            <input type="text" class="input" placeholder="Enter Last Name" name="name" required oninvalid="this.setCustomValidity('Please Enter Your Last Name')"
            oninput="this.setCustomValidity('')"/>
            <br />
            <label for="email" class="fs-5">Email Account</label>
            <br />
            <input
              name="Email"
              id="email"
              type="email"
              class="input"
              placeholder="example@gmail.com"
                required
              oninvalid="this.setCustomValidity('Please Enter Your Email Address')"
              oninput="this.setCustomValidity('')"
            />
            <br />
            <label for="" class="fs-5">Leave Us a Message</label>
            <br />
            <input type="text" class="inputmess" name="text" required oninvalid="this.setCustomValidity('Message Required')"
            oninput="this.setCustomValidity('')"/>
            <br />
            <br />
            <center>
            <button class="box1" type="reset"><span class="text-white">Clear</span></button> <br>
            
            <button type="submit">
              <span class="box text-white"> Send! </span>
            </button>
            </center>
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
  cursor: pointer !important;
  font-size: 1rem !important;
}

.pad:hover {
  transform: scale(1.05) !important;
  transition: ease-in 0.5s !important;
}

.colbrd {
    border-right: white solid !important;
}

.input {
  border-radius: 1.5rem !important;
  width: 16rem !important;
  height: 2.8rem !important;
}

input:hover {
    box-shadow: #ffffff 0px 0px 8px 8px !important;
    cursor: pointer !important;
}

.inputmess {
  border-radius: 1.5rem !important;
  height: 5.8rem !important;
  width: 16rem !important;
}

.box {
  width: 140px !important;
  height: auto !important;
  float: left !important;
  transition: .5s linear !important;
  position: relative !important;
  display: block !important;
  overflow: hidden !important;
  padding: 15px !important;
  text-align: center !important;
  margin: 0 5px !important;
  background: transparent !important;
  text-transform: uppercase !important;
  font-weight: 900 !important;
}

.box:before {
  position: absolute !important;
  content: '' !important;
  left: 0 !important;
  bottom: 0!important;
  height: 4px!important;
  width: 100%!important;
  border-bottom: 4px solid transparent!important;
  border-left: 4px solid transparent!important;
  box-sizing: border-box!important;
  transform: translateX(100%)!important;
}

.box:after {
  position: absolute!important;
  content: ''!important;
  top: 0!important;
  left: 0!important;
  width: 100%!important;
  height: 4px!important;
  border-top: 4px solid transparent!important;
  border-right: 4px solid transparent!important;
  box-sizing: border-box!important;
  transform: translateX(-100%)!important;
}

.box:hover {
  box-shadow: 0 5px 25px rgb(23, 0, 128) !important;
}

.box:hover:before {
  border-color: #00eaff!important;
  height: 100%!important;
  transform: translateX(0)!important;
  transition: .3s transform linear, .3s height linear .3s!important;
}

.box:hover:after {
  border-color: #ffffff!important;
  height: 100%!important;
  transform: translateX(0)!important;
  transition: .3s transform linear, .3s height linear .5s!important;
}

.box1 {
  width: 140px !important;
  height: auto !important;
  transition: .5s linear !important;
  position: relative !important;
  display: block !important;
  overflow: hidden !important;
  padding: 15px !important;
  text-align: center !important;
  margin: 0 5px !important;
  background: transparent !important;
  text-transform: uppercase !important;
  font-weight: 900 !important;
}

.box1:before {
  position: absolute !important;
  content: '' !important;
  left: 0 !important;
  bottom: 0!important;
  height: 4px!important;
  width: 100%!important;
  border-bottom: 4px solid transparent!important;
  border-left: 4px solid transparent!important;
  box-sizing: border-box!important;
  transform: translateX(100%)!important;
}

.box1:after {
  position: absolute!important;
  content: ''!important;
  top: 0!important;
  left: 0!important;
  width: 100%!important;
  height: 4px!important;
  border-top: 4px solid transparent!important;
  border-right: 4px solid transparent!important;
  box-sizing: border-box!important;
  transform: translateX(-100%)!important;
}

.box1:hover {
  box-shadow: 0 5px 25px rgb(23, 0, 128) !important;
}

.box1:hover:before {
  border-color: #00eaff!important;
  height: 100%!important;
  transform: translateX(0)!important;
  transition: .3s transform linear, .3s height linear .3s!important;
}

.box1:hover:after {
  border-color: #ffffff!important;
  height: 100%!important;
  transform: translateX(0)!important;
  transition: .3s transform linear, .3s height linear .5s!important;
}

button {
  color: black!important;
  text-decoration: none!important;
  cursor: pointer!important;
  outline: none!important;
  border: none!important;
  background: transparent!important;
}

@media (width <= 300px) {
    .pad {
        font-size: 9px !important;
        font-weight: 400;
    }
    .input {
        font-size: 7px !important;
        width: 6.4rem !important;
        height: 1.6rem !important;
    }
    .inputmess {
        font-size: 7px !important;
        width: 6.4rem !important;
        height: 3rem !important;
    }
    label {
        font-size: 12px !important;
    }
    .box {
        width: 65px;
        height: 20px;
        font-size: 12px;
    }
    .box1 {
        width: 65px;
        height: 20px;
        font-size: 12px;
    }
    .colbrd {
    border-right: white solid .1px;
}
}
</style>
