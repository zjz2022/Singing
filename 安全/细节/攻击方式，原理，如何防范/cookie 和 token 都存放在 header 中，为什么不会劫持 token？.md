cookie 和 token 都存放在 header 中，为什么不会劫持 token？



1、首先token不是防止XSS的，而是为了防止CSRF的；
2、CSRF攻击的原因是浏览器会自动带上cookie，而浏览器不会自动带上token