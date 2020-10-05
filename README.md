<style>
  .custom-checkbox{}
  .custom-checkbox__label {
    display: inline-flex;
    align-items: center;
    cursor: pointer;
  }
  
  .custom-checkbox__base {
    position: absolute;
    width: 0;
    height: 0;
    opacity: 0;
  }
  
  .custom-checkbox__new {
    position: relative;
    display: inline-block;
    width: 20px;
    height: 20px;
    border: 1px solid orange;
    overflow: hidden;
    transition: all .15s linear;
  }

  .custom-checkbox__new::before {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    content: '';
    display: block;
    width: 15px;
    height: 15px;
    /*background: url("./check.png") no-repeat center center;*/
    /*background-size: cover;*/
    background-color: orange;
    transition: all .15s linear;
  }

  .custom-checkbox__base:checked + .custom-checkbox__new::before {
    transform: translate(-50%, -50%) scale(1);
  }

  .custom-checkbox__base:focus + .custom-checkbox__new {
    border: 1px solid orangered;
  }

  .custom-checkbox__text {
    padding: 0 5px;
    font-size: 20px;
  }

  /****************************************************************/

  .custom-radio{
    margin-bottom: 5px;
  }
  .custom-radio__label {
    display: inline-flex;
    align-items: center;
    cursor: pointer;
  }

  .custom-radio__base {
    position: absolute;
    width: 0;
    height: 0;
    opacity: 0;
  }

  .custom-radio__new {
    position: relative;
    display: inline-block;
    width: 20px;
    height: 20px;
    border: 1px solid orange;
    border-radius: 50%;
    overflow: hidden;
    transition: all .15s linear;
  }

  .custom-radio__new::before {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    content: '';
    display: block;
    width: 13px;
    height: 13px;
    background-color: orange;
    border-radius: inherit;
    transition: all .15s linear;
  }

  .custom-radio__base:checked + .custom-radio__new::before {
    transform: translate(-50%, -50%) scale(1);
  }

  .custom-radio__base:focus + .custom-radio__new {
    border: 1px solid orangered;
  }
  
  .custom-radio__text {
    padding: 0 5px;
    font-size: 20px;
  }
  
</style>

<div class="custom-checkbox">
  <label class="custom-checkbox__label">
    <input class="custom-checkbox__base" type="checkbox" name="">
    <span class="custom-checkbox__new"></span>
    <span class="custom-checkbox__text">Checkbox 1</span>
  </label>
</div>

<hr>

<div class="custom-checkbox">
  <label class="custom-checkbox__label">
    <span class="custom-checkbox__text">Checkbox 1</span>
    <input class="custom-checkbox__base" type="checkbox" name="">
    <span class="custom-checkbox__new"></span>
  </label>
</div>

<hr>

<div class="custom-radio">
  <label class="custom-radio__label">
    <input class="custom-radio__base" type="radio" name="radio" value="1" checked>
    <span class="custom-radio__new"></span>
    <span class="custom-radio__text">Radio 1</span>
  </label>
</div>
<div class="custom-radio">
  <label class="custom-radio__label">
    <input class="custom-radio__base" type="radio" name="radio" value="2">
    <span class="custom-radio__new"></span>
    <span class="custom-radio__text">Radio 2</span>
  </label>
</div>

<hr>

<div class="custom-radio">
  <label class="custom-radio__label">
    <span class="custom-radio__text">Radio 1</span>
    <input class="custom-radio__base" type="radio" name="radio-1" value="1" checked>
    <span class="custom-radio__new"></span>
  </label>
</div>
<div class="custom-radio">
  <label class="custom-radio__label">
    <span class="custom-radio__text">Radio 2</span>
    <input class="custom-radio__base" type="radio" name="radio-1" value="2">
    <span class="custom-radio__new"></span>
  </label>
</div>
