<style>

  .section {
    display: flex;
    padding-bottom: 100px;
  }

  h2 {
    text-align: left;
    margin: 0;
    margin-top: 50px;
    margin-left: 25px;
    margin-bottom: 25px;
  }

  .line {
    position: relative;
    height: 1px;
    background-color: var(--primary-dark);
    margin: 25px 25px 50px 25px;
  }

  .img-wrapper {
    flex: 4;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 25px;
    height: 500px;
    overflow: hidden;
  }

  img {
    width: 100%;
    height: auto;
  }

  .form-wrapper {
    flex: 5;
    padding: 25px;
  }

  .fcf-input-group {
    position: relative;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -ms-flex-align: stretch;
    align-items: stretch;
    width: 100%;
  }

  .fcf-form-control {
      display: block;
      width: 100%;
      height: calc(1.5em + 0.75rem + 2px);
      padding: 0.375rem 0.75rem;
      font-size: 1rem;
      font-weight: 400;
      line-height: 1.5;
      color: #495057;
      background-color: #fff;
      background-clip: padding-box;
      border: 1px solid #ced4da;
      outline: none;
      border-radius: 0.25rem;
      transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
  }

  .fcf-form-group {
    text-align: left;
  }

  .fcf-form-control:focus {
      border: 1px solid #313131;
  }

  select.fcf-form-control[size], select.fcf-form-control[multiple] {
      height: auto;
  }

  textarea.fcf-form-control {
      font-family: -apple-system, Arial, sans-serif;
      height: auto;
  }

  label.fcf-label {
      display: inline-block;
      margin-bottom: 0.5rem;
  }

  .fcf-credit {
      padding-top: 10px;
      font-size: 0.9rem;
      color: #545b62;
  }

  .fcf-credit a {
      color: #545b62;
      text-decoration: underline;
  }

  .fcf-credit a:hover {
      color: #0056b3;
      text-decoration: underline;
  }

  .fcf-btn {
      display: inline-block;
      font-weight: 400;
      color: #212529;
      text-align: center;
      vertical-align: middle;
      cursor: pointer;
      -webkit-user-select: none;
      -moz-user-select: none;
      -ms-user-select: none;
      user-select: none;
      background-color: transparent;
      border: 1px solid transparent;
      padding: 0.375rem 0.75rem;
      font-size: 1rem;
      line-height: 1.5;
      border-radius: 0.25rem;
      transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
  }

  @media (prefers-reduced-motion: reduce) {
      .fcf-btn {
          transition: none;
      }
  }

  .fcf-btn:hover {
      color: #212529;
      text-decoration: none;
  }

  .fcf-btn:focus, .fcf-btn.focus {
      outline: 0;
      box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
  }

  .fcf-btn-primary {
      color: #fff;
      background-color: var(--primary-text);
      border-color: var(--primary-text);
  }

  .fcf-btn-primary:hover {
      color: #fff;
      background-color: var(--secondary-text);
      border-color: var(--secondary-text);
  }

  .fcf-btn-primary:focus, .fcf-btn-primary.focus {
      color: #fff;
      background-color: #0069d9;
      border-color: #0062cc;
      box-shadow: 0 0 0 0.2rem rgba(38, 143, 255, 0.5);
  }

  .fcf-btn-lg, .fcf-btn-group-lg>.fcf-btn {
      padding: 0.5rem 1rem;
      font-size: 1.25rem;
      line-height: 1.5;
      border-radius: 0.3rem;
  }

  .fcf-btn-block {
      display: block;
      width: 100%;
  }

  .fcf-btn-block+.fcf-btn-block {
      margin-top: 0.5rem;
  }

  input[type="submit"].fcf-btn-block, input[type="reset"].fcf-btn-block, input[type="button"].fcf-btn-block {
      width: 100%;
  }
</style>


<h2>Hit me up!</h2>
<div class='line' />


<div class='section' id='contact'>

  <div class='img-wrapper'>
    <img src='https://i.etsystatic.com/21824466/r/il/f1bd7f/2647818173/il_1588xN.2647818173_geox.jpg' alt='disco-hanger' />
  </div>


  <div class='form-wrapper'>
    <div class="fcf-body">
      
      <div id="fcf-form">

      <form id="fcf-form-id" class="fcf-form-class" method="post" action="mailto:perpetualhang@gmail.com">
          
          <div class="fcf-form-group">
              <label for="Name" class="fcf-label">Your name</label>
              <div class="fcf-input-group">
                  <input type="text" id="Name" name="Name" class="fcf-form-control" required>
              </div>
          </div>

          <div class="fcf-form-group">
              <label for="Email" class="fcf-label">Your email address</label>
              <div class="fcf-input-group">
                  <input type="email" id="Email" name="Email" class="fcf-form-control" required>
              </div>
          </div>

          <div class="fcf-form-group">
              <label for="Message" class="fcf-label">Your message</label>
              <div class="fcf-input-group">
                  <textarea id="Message" name="Message" class="fcf-form-control" rows="9" maxlength="3000" required></textarea>
              </div>
          </div>

          <div class="fcf-form-group">
              <button type="submit" id="fcf-button" class="fcf-btn fcf-btn-primary fcf-btn-lg fcf-btn-block">Send Message</button>
          </div>

      </form>
      </div>
    </div>
  </div>
</div>