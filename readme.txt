this is my practice project of localization of laravel
this is my summary of the project


--------------------web.php --------------------

Route::get('profile/{lang}',function($lang){
    App::setlocale($lang);
    return view('profile');
});


--------------------------------------------



------------------profile.blade.php-----------------


<div style="display: flex;justify-content:center;align-items:center;flex-direction:column">
<h1>{{__('profile.welcome')}}</h1>

<div>
    <a href="">{{__('profile.about')}}</a>
    <a href="">{{__('profile.contact')}}</a>
    <a href="">{{__('profile.list')}}</a>
</div>
<div>
    <br>
    <br>
    <a href="/profile/en">Change to english</button>
    <a href="/profile/ne">नेपालीमा परिवर्तन</button>

</div>
</div>

--------------------------------------------------------------

--------------- lang/ne/profile.php------------------------------

<?php
return [
    "welcome"=>"प्रोफाइल पेजमा स्वागत छ",
    "about"=>"बारेमा",
    "list"=>"सूची",
    "contact"=>"सम्पर्क गर्नुहोस्"
];
?>
--------------------------------------------------

