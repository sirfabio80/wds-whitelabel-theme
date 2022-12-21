# wds-whitelabel-theme
WDS Whitelabel Theme

The theme will be applied on top of the OOB Polaris base one through the System Property **glide.ui.polaris.theme.custom**

Further info can be found on [Docs](https://docs.servicenow.com/bundle/tokyo-platform-user-interface/page/administer/navigation-and-ui/task/config-next-experience-themes-prefs.html)

![screenshot](https://user-images.githubusercontent.com/26232376/208645069-e35ea523-4016-4d05-a149-cd2607c03c84.jpg)

# Instructions after installation
                
1. A fictional company logo (**solana.png**) is available to download (System UI &gt; Images &gt; **x_snc_wds_wl_theme.solana.png** or from URL *instanceName*/nav_to.do?uri=db_image.do?sys_id=6ff51953c3ff51103115fe94e40131a8 )

![solana](https://user-images.githubusercontent.com/26232376/208886162-9fef5b26-5c06-4c76-907e-1a03eef18869.png)

2. Load the downloaded image, from the previous point or your favourite one, onto the system property **glide.product.image.light**. More info on [Docs](https://docs.servicenow.com/bundle/tokyo-platform-user-interface/page/administer/navigation-and-ui/task/t_ConfigureLogoColorsSysDfltsUI16.html)

3. [Optional for custom Service Portal based on Employee Center] At the bottom of the Employee Center theme variables, please append the following ones:

```scss
//== Overriding for Solana
$border-radius-base:        3px;
$border-radius-large:       8px;
$border-radius-small:       2px;
$panel-border-radius: $border-radius-large;
$nav-pills-border-radius: $border-radius-base !default;
$btn-border-radius-base: $border-radius-base;
$btn-border-radius-large: $border-radius-base;
$btn-border-radius-small: $border-radius-base;
$input-color-placeholder: #525762;

//== Solana Typography
$font-size-base: 14px;
$font-size-3xl: ceil(($font-size-base * 2.25)); // 36px New
$font-size-xxl: ceil(($font-size-base * 1.875)); // 30px  New
$font-size-xl: ceil(($font-size-base * 1.5)); // 24px New
$font-size-large: ceil(($font-size-base * 1.25)); // 20px  
$font-size-md: $font-size-base; // 16px New
$font-size-small: ceil(($font-size-base * 0.875)); // 14px
$font-size-xs: ceil(($font-size-base * 0.75)); // 12px New 
$font-size-h1: ceil(($font-size-base * 2)); // 32px 
$font-size-h2: ceil(($font-size-base * 1.5)); // 24px 
$font-size-h3: ceil(($font-size-base * 1.25)); // 20px 
$font-size-h4: ceil(($font-size-base * 1.125)); // 18px 
$font-size-h5: $font-size-base;
$font-size-h6: ceil(($font-size-base * 0.875)); // 14px  

//== Solana Forms
$padding-base-vertical:     10px !default;
$padding-base-horizontal:   14px !default;
$padding-large-vertical:    12px !default;
$padding-large-horizontal:  16px !default;
$padding-small-vertical:    6px !default;
$padding-small-horizontal:  10px !default;
$input-height-base: 42px;
$input-border: transparent;
$input-group-addon-border-color: $input-border;
$input-bg-disabled: #f6f6f8;
$x_snc_wds_wl_theme-form-label: #181A1F;

//== Solana others
$sp-navbar-height: 62px;
$headings-font-weight:    700;
$headings-line-height:    1.1;
$headings-color:          #000000;
$link-color: #049DC2;
$badge-active-color: $link-color;
$pagination-color: $link-color;
$input-border-focus: $link-color;

```

4. Add with higher order (so to be loaded for last) the stylesheet includend in the scope app with name **x_snc_wds_wl_theme_utils.css** to your choosen theme.
