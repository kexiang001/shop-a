<template>
  <div class="hello">
    <nav-bread>
        注册
    </nav-bread>
    <div class="register_wrap">
        <div class="bugfix_ie6 dis_none">
            <div class="n-logo-area clearfix">
                <a href="http://mi.shudong.wang/" class="fl-l"><img src="/static/img/vn-logo.png" width="260"></a>
            </div>
        </div>
        <div id="main">
            <div class="n-frame device-frame reg_frame">

                <div class="title-item dis_bot35 t_c">
                    <h4 class="title-big">注册格美官网帐号 </h4>
                </div>
                <div class="regbox" id="register_box">
                    <form action="http://mi.shudong.wang/user.php" method="post" name="formUser" onsubmit="return register();">
                        <input type="hidden" value="C4E1AB9A7DE79D7C750E8916875E7DBE" id="validate">
                        <div class="phone_step1">
                            <input type="hidden" id="sendtype">

                            <div class="inputbg">
                                <label class="labelbox">
                      <input type="text" name="username" id="username" onblur="is_registered(this.value);" onkeyup="is_registered(this.value);" placeholder="用户名">
                  </label>
                                <span class="t_text">用户名</span>
                                <span class="error_icon"></span>
                            </div>
                            <div class="err_tip" id="username_notice"> <em></em> </div>

                            <div class="inputbg">
                                <label class="labelbox">
                      <input name="email" type="text" id="email" onblur="checkEmail(this.value);" onkeyup="checkEmail(this.value);" placeholder="email">
                  </label>
                                <span class="t_text">email</span>
                                <span class="error_icon"></span>
                            </div>
                            <div class="err_tip" id="email_notice"><em></em> </div>

                            <div class="inputbg">
                                <label class="labelbox">
                  <input type="password" name="password" id="password1" onblur="check_password(this.value);" onkeyup="check_password(this.value);checkIntensity(this.value);" placeholder="密码">
                  </label>
                                <span class="t_text">密码</span>
                                <span class="error_icon"></span>
                            </div>
                            <div class="err_tip" id="password_notice"> <em></em> </div>

                            <div class="inputbg">
                                <label class="labelbox">
                    <input name="confirm_password" type="password" id="conform_password" onblur="check_conform_password(this.value);" onkeyup="check_conform_password(this.value);" placeholder="确认密码">
                  </label>
                                <span class="t_text">确认密码</span>
                                <span class="error_icon"></span>
                            </div>
                            <div class="err_tip" id="conform_password_notice"> <em></em> </div>



                            <div class="inputbg inputcode dis_box clearfix">
                                <label class="labelbox label-code">
                      <input type="text" class="code" name="captcha" maxlength="6" placeholder="验证码">
                  </label>
                                <span class="t_text">验证码</span>
                                <span class="error_icon"></span>
                                <img src="http://mi.shudong.wang/captcha.php?148237837" alt="captcha" class="icode_image code-image chkcode_img" onclick="this.src='captcha.php?'+Math.random()">
                            </div>
                            <div class="err_tip"> <em></em> </div>
                            <div class="law">
                                <label>
                    <input name="agreement" type="checkbox" value="1" checked="checked" tabindex="5" class="remember-me">
                    我已看过并接受《<a href="http://mi.shudong.wang/article.php?cat_id=-1" style="color:blue" target="_blank">用户协议</a>》</label>
                            </div>
                            <div class="err_tip"> <em></em> </div>
                            <div class="fixed_bot mar_phone_dis1">
                                <input name="act" type="hidden" value="act_register">
                                <input type="hidden" name="back_act" value="">
                                <input name="Submit" type="submit" value="同意协议并注册" class="btn332 btn_reg_1 submit-step">
                            </div>
                            <div class="trig">已有账号? <a href="http://mi.shudong.wang/user.php" class="trigger-box">点击登录</a> </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
        <div class="n-footer">
            <div class="nl-f-nav">
                <span>
                        </span>
            </div>
            <p class="nf-intro"><span>©<a href="http://mi.shudong.wang/user.php?act=register#">vnshop.cn</a> 京ICP证110507号 京ICP备10046444号 京公网安备1101080212535号 <a href="http://mi.shudong.wang/user.php?act=register#">京网文[2014]0059-0009号</a></span></p>
        </div>
    </div>
    
    
  </div>
</template>

<script>

import NavBread from '@/components/NavBread'
export default {
  name: 'Register',
  components:{
    NavBread
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
     .input-sub,
        .input-add {
            min-width: 40px;
            height: 100%;
            border: 0;
            color: #605F5F;
            text-align: center;
            font-size: 16px;
            overflow: hidden;
            display: inline-block;
            background: #f0f0f0;
        }
        
        .item-quantity .select-self-area {
            background: none;
            border: 1px solid #f0f0f0;
        }
        
        .item-quantity .select-self-area .select-ipt {
            display: inline-block;
            padding: 0 3px;
            width: 30px;
            min-width: 30px;
            text-align: center;
        }
</style>
