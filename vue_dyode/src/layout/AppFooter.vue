<template>
    <footer class="footer has-cards">
    <div class="container" style="padding-top: 20px;padding-left:30px; background: #000000; color:white;margin-top:-80px;">
        <b-row>
            <b-col md="2">
                <h6 style="font-family:Pacifico;line-height:0.7cm; color:white;">Customer Service</h6>
                <p style="font-size:13px; font-family:Lato; line-height:0.2cm;">Accessibility</p>
                <p style="font-size:13px; font-family:Lato; line-height:0.2cm;">Contact Us</p>
                <p style="font-size:13px; font-family:Lato; line-height:0.2cm;">Return Policy</p>
                <p style="font-size:13px; font-family:Lato; line-height:0.2cm;">FAQ</p>
                <p style="font-size:13px; font-family:Lato; line-height:0.2cm;">Gift Certificates</p>
                <p style="font-size:13px; font-family:Lato; line-height:0.2cm;">Wishlist</p>
            </b-col>
            <b-col md="7">
                <h6 style="font-family:Pacifico;line-height:0.7cm; color:white;">Company</h6>
                <p style="font-size:13px; font-family:Lato;line-height:0.2cm;">About Us</p>
                <p style="font-size:13px; font-family:Lato;line-height:0.2cm;">Careers</p>
                <p style="font-size:13px; font-family:Lato;line-height:0.2cm;">Press</p>
                <p style="font-size:13px; font-family:Lato;line-height:0.2cm;">Affiliates</p>
            </b-col>
            <b-col md="2" style="margin-left:7%;">
                <h6 style="font-family:Pacifico;line-height:0.7cm; color:white;">Follow Us</h6>
                <div class="footer-right">
                    <b-img src="img/img/Group_1.png" alt="Email Icon" ></b-img>
                    <b-img src="img/img/Group_2.png" alt="Email Icon" style="margin-left:10%;"></b-img>
                    <b-img src="img/img/Group_3.png" alt="Email Icon" style="margin-left:10%;"></b-img>
                </div>
            </b-col>
        </b-row>
    </div>
    </footer>
</template>
<script>
export default {
  name: 'app-footer',
  data() {
    return {
      year: new Date().getFullYear()
    }
  }
};
</script>
<style>
</style>
