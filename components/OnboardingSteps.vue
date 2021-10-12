<template>
    <div class="steps-container">
        <div class="content">
           
            <span class="content-number">1</span>
            <span class="content-text">Verify Account</span>
        </div>

         <div class="content">
            <span class="content-number">2</span>
            <span class="content-text">Social Handles</span>
        </div>

         <div class="content">
            <span class="content-number">3</span>
            <span class="content-text">Business Categories</span>
        </div>
        
        

    </div>
</template>

<script></script>

<style lang="scss">
.steps-container {
  display: flex;
  align-items: center;
  flex-direction: row;
  margin-top: 0.3rem;

  .content {
      display: flex;
      align-items: baseline;
      margin-right: 45px;
    }

  .content-number {
      height: 40px;
      width: 40px;
      flex-grow: 1;
      background-color: #006AFF;
      border-radius: 3px;
      color:#FFF;
      font-weight: 700;
      font-size: 16px;
      line-height: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      }

      .content-text {
          display: none;
          margin-left: 0.5rem;
          @media (min-width: 992px) {
            display: block !important;
        }
    }

}

</style>