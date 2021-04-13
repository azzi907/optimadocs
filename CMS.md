---
id: Cms
title: Cms Model
---

path : src/models/Cms.php

## Site Settings

> * get array of settings

Example Usage : 
```php
/**
 * @return    array               Data
 */

use optima\models\Cms;

$settings = Cms::settings();

```
Example Output:

```phparray
Array
(
    [_id] => 5dc512f1b15da70f29012cd1
    [number_custom_settings] => 5
    [custom_settings] => Array
        (
            [0] => Array
                (
                    [type] => input
                    [key] => facebook
                    [value] => https://www.facebook.com/xxxx/
                )

            [1] => Array
                (
                    [type] => input
                    [key] => mail
                    [value] => INFO@xxxx.COMs
                )
        )

    [template_url] => 
    [general_settings] => Array
        (
            [site_title] => 3SA Estate
            [admin_email] => admin@xxx.optimasit.com
            [show_watermark] => 1
        )

    [site_id] => 120
    [agency] => 5d971b78b15da701ad5a2023
    [created_by] => 5d971ce2b15da706776bb1f9
    [created_at] => 2019-11-08T08:02:09+01:00
    [frontend_settings] => Array
        (
            [0] => Array
                (
                    [setting_key] => 
                    [type] => other
                )

        )

    [header] => Array
        (
            [logo] => Array
                (
                    [name] => 3sa_logga_koppar (2).png
                )

        )

    [updated_at] => 2019-11-14T09:09:51+01:00
    [updated_by] => 5d971c9ab15da7278c205eb8
)

```
## Site Custom Settings

> * get array of custom settings

Example Usage : 
```php
/**
 * @return    array               Data
 */

use optima\models\Cms;

$custom_settings = Cms::custom_settings();

```
Example Output:

```phparray
Array
(
    [Instagram] => https://www.instagram.com/ibizaestates/
    [Facebook] => https://www.facebook.com/ibizaestatesnl/
    [Pinterest] => https://nl.pinterest.com/ibizaestates/
    [Youtube] => https://www.youtube.com/channel/UCFfDO1HKlliOBeOO6Lcn-9w/featured
    [Twitter] => https://twitter.com/Ibiza_estates
    [Linkedin] => https://www.linkedin.com/company/ibiza-estates
)

```
## Page/Post Custom Settings

> * get array of page/post custom settings

Example Usage : 
```php
/**
 * @param     array  $page_data['custom_settings'] OR $post['custom_settings']
 *
 *
 * @return    array               Data
 */

use optima\models\Cms;

/* For page */
$page_custom_settings = Cms::custom_settings($page_data['custom_settings']);

/* For post */
$post_custom_settings = Cms::custom_settings($post['custom_settings']);

```
Example Output:

```phparray
Array
(
    [Instagram] => https://www.instagram.com/ibizaestates/
    [Facebook] => https://www.facebook.com/ibizaestatesnl/
    [Pinterest] => https://nl.pinterest.com/ibizaestates/
    [Youtube] => https://www.youtube.com/channel/UCFfDO1HKlliOBeOO6Lcn-9w/featured
    [Twitter] => https://twitter.com/Ibiza_estates
    [Linkedin] => https://www.linkedin.com/company/ibiza-estates
)

```
## Translations

> * Used mostly /messages/{lang}/app.php file

> get array of translations

Example Usage : 

```php
/**
 * @return    array               Data
 */

use optima\models\Cms;

$translations = Cms::getTranslations();

```
Example Output:

```phparray
Array
(
    [beachfront] => Array
        (
            [_id] => Array
                (
                    [$oid] => 5ddcc5abb15da76aee2f5bc2
                )

            [key] => beachfront
            [site_id] => 112
            [value] => Beachfront
            [created_by] => 5abe17258280de6f08659dc6
            [agency] => 5abe15f48280de6f6150c895
            [language] => EN
            [status] => completed
            [created_at] => 2019-11-26T07:26:51+01:00
            [updated_at] => 2019-12-02T12:41:14+01:00
            [updated_by] => 5d49902ab15da74df0537262
        )
)

```
## Menus

> * get array of menus

Example Usage : 
```php
/**
 * @param     string  $menuName   it is the name of menu in CRM
 *
 *
 * @return    array               Data
 */

use optima\models\Cms;

$menu = Cms::menu($menuName);

```
Example Output:

```phparray
Array
(
    [_id] => 5dad78b2b15da748572bcd11
    [name] => Array
        (
            [EN] => Menu
            [NL] => Menu
            [DE] => Menu
        )

    [site_id] => 112
    [agency] => 5abe15f48280de6f6150c895
    [created_by] => 5abe179c8280de702d6fe496
    [created_at] => 2019-10-21T11:21:54+02:00
    [key] => 237
    [menu_items] => Array
        (
            [0] => Array
                (
                    [item] => Array
                        (
                            [title] => Array
                                (
                                    [EN] => PROPERTIES
                                    [NL] => AANBOD
                                    [DE] => EIGENSCHAFTEN
                                )

                            [slug] => Array
                                (
                                    [EN] => ibiza-real-estate
                                    [ES] => /properties
                                    [NL] => ibiza-real-estate
                                    [DE] => hauser-kaufen-ibiza
                                )

                            [id] => 5dad78b2b15da748572bcd11
                        )

                )

        )

    [updated_at] => 2019-12-09T11:19:03+01:00
    [updated_by] => 5abe17258280de6f08659dc6
)

```
## CRM Active Languages

> * get array of languages

Example Usage : 
```php
/**
 * @return    array               Data
 */

use optima\models\Cms;

$languages = Cms::languages();

```
Example Output:

```phparray
Array
(
    [0] => Array
        (
            [_id] => 57c67313f06e856b2016ee94
            [title] => English
            [key] => EN
            [agency] => 56b06e4d2bc1d95f60cedef2
            [created_by] => 5623e6cf9d6388636b655866
            [created_at] => 2016-08-31T06:02:59+00:00
            [updated_at] => 2018-02-28T13:04:07+01:00
            [updated_by] => 58a5ab68f06e85b06cb4f6ce
            [site_id] => 9
        )
)

```
## CRM System Languages

> * Used mostly to coordinate between System and Active languages for getting data from API response

> * get array of System Languages

Example Usage : 
```php
/**
 * @return    array
 */

use optima\models\Cms;

$system_languges = Cms::SystemLanguages();

```
Example Output:

```phparray
Array
(
    [0] => Array
        (
            [_id] => 56b1d99d2bc1d9c562cedef2
            [for] => System
            [key] => EN
            [value] => Array
                (
                    [en] => English
                    [es_AR] => Inglés
                )

            [status] => Active
            [created_by] => 5623e6cf9d6388636b655866
            [agency] => 56b06e4d2bc1d95f60cedef2
            [updated_by] => 57d2464af06e857a29f365c7
            [internal_key] => EN
        )
)

```
## Categories

> * get array of Categories (Created in CMS)

Example Usage : 
```php
/**
 * @return    array
 */

use optima\models\Cms;

$categories = Cms::Categories();

```
Example Output:

```phparray
Array
(
    [0] => Array
        (
            [_id] => 5dfb781db15da710393fd437
            [type] => category
            [name] => test
            [slug] => test-slug
            [desc] => test desc
            [site_id] => 112
            [agency] => 5abe15f48280de6f6150c895
            [created_by] => 5abe17258280de6f08659dc6
            [created_at] => 2019-12-19T14:16:13+01:00
        )

)
```

## Page/Post by Slug

> * get array of page/post

Example Usage : 
```php
/**
 * @param    string  $slug        slug of page/post type
 * @param    string  $lang_slug   language for page/post type
 * @param    string  $id          GET page/post type by mongo ObjectId e.g "507f191e810c19729de860ea"
 * @param    string  $type        type for getting page OR post
 * @return    array               Data
 */

use optima\models\Cms;

$page_data = pageBySlug($slug, $lang_slug = 'EN', $id = null, $type = 'page')

```
Example Output:

```phparray
Array
(
    [featured_image] => 
    [featured_image_200] => 
    [content] => 
    [title] => Home
    [slug] => home
    [slug_all] => Array
        (
            [EN] => home
            [ES] => home
            [NL] => home
            [DE] => home
        )

    [meta_title] => Experienced real estate agency in Ibiza
    [meta_desc] => Buying or selling a property in Ibiza? Ibiza Estates is an experienced real estate agency in Ibiza. Take a look at our luxury properties, villas and houses for sale in Ibiza.
    [meta_keywords] => ibiza estates, ibiza estate real estate agency, ibiza real estate agency, real estate ibiza, best real estate agency ibiza, ibiza real estate, exclusive ibiza properties, luxury villas ibiza, luxury apartments ibiza, luxury villa ibiza, luxury apartment ibiza, luxury property in ibiza, luxury home in ibiza
    [custom_settings] => Array
        (
            [EN] => Array
                (
                    [0] => Array
                        (
                            [key] => bg_img5
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img.jpg
                        )

                    [1] => Array
                        (
                            [key] => bg_img4
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img1.jpg
                        )

                    [2] => Array
                        (
                            [key] => bg_img3
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img2.jpg
                        )

                    [3] => Array
                        (
                            [key] => bg_img2
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112336000000_img3.jpg
                        )

                    [4] => Array
                        (
                            [key] => bg_img1
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112337000000_img4.jpg
                        )

                )

            [NL] => Array
                (
                    [0] => Array
                        (
                            [key] => bg_img5
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img.jpg
                        )

                    [1] => Array
                        (
                            [key] => bg_img4
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img1.jpg
                        )

                    [2] => Array
                        (
                            [key] => bg_img3
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img2.jpg
                        )

                    [3] => Array
                        (
                            [key] => bg_img2
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112336000000_img3.jpg
                        )

                    [4] => Array
                        (
                            [key] => bg_img1
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112337000000_img4.jpg
                        )

                )

            [DE] => Array
                (
                    [0] => Array
                        (
                            [key] => bg_img5
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img.jpg
                        )

                    [1] => Array
                        (
                            [key] => bg_img4
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img1.jpg
                        )

                    [2] => Array
                        (
                            [key] => bg_img3
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112335000000_img2.jpg
                        )

                    [3] => Array
                        (
                            [key] => bg_img2
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112336000000_img3.jpg
                        )

                    [4] => Array
                        (
                            [key] => bg_img1
                            [value] => https://images.optima-crm.com/cms_medias/112/20191115112337000000_img4.jpg
                        )

                )

        )

    [created_at] => 2019-10-17T12:15:55+02:00
)
```
## Page/Post by Id

> * get array of page/post

Example Usage : 
```php
/**
 * @param    string  $id          Get page/post by mongo Object Id e.g "507f191e810c19729de860ea"
 *
 *
 * @return    array               Data
 */

use optima\models\Cms;

$page_data = Cms::postById($id);

```
Example Output:

```phparray
Array
(
    [featured_image] => 
    [featured_image_200] => 
    [content] => San Antonio Een huis kopen in San Antonio ofwel San Antonio de Portmany heeft veel voordelen. Deze kant van Ibiza wordt ook wel de sunset coast genoemd. Wanneer u naar woningen te koop in San Antonio zoekt, bent u verzekerd van een schitterende zonsondergang. Naast dit feit vindt u in de tweede stad van Ibiza veel voorzieningen. Wanneer u een huis in San Antonio gevonden heeft, hoeft u slechts tien minuten te rijden voor de mooiste én meest bekende stranden van Ibiza. Cala Conta en Cala Bassa bereikt u zo vanuit San Antonio. Ook de verbinding met Ibiza-stad is gunstig te noemen. San Antonio en Ibiza-stad worden met elkaar verbonden door de enige snelweg die het eiland telt.   


    [title] => San Antonio
    [slug] => huis-kopen-san-antonio
    [slug_all] => Array
        (
            [EN] => san-antonio-property-for-sale
            [NL] => huis-kopen-san-antonio
            [DE] => haus-kaufen-san-antonio
        )

    [meta_title] => Huis kopen op Ibiza in San Antonio
    [meta_desc] => Huis kopen Ibiza, deze woningen staan te koop in de regio San Antonio. Bekijk het aanbod van villa's, appartementen en huizen te koop in San Antonio, Ibiza.
    [meta_keywords] => onroerend goed kopen in san antonio, onroerend goed kopen san antonio, kopen van een huis san antonio, kopen van huis san antonio, onroerend goed te koop san antonio
    [custom_settings] => Array
        (
            [EN] => Array
                (
                    [0] => Array
                        (
                            [key] => lg_by_key
                            [value] => 578
                        )

                )

            [NL] => Array
                (
                    [0] => Array
                        (
                            [key] => lg_by_key
                            [value] => 578
                        )

                )

            [DE] => Array
                (
                    [0] => Array
                        (
                            [key] => lg_by_key
                            [value] => 578
                        )

                )

        )

    [created_at] => 2019-11-22T06:03:01+01:00
)
```
## Render Page View

> * get view of page if found otherwise 404 page will be rendered

Example Usage : 
```php
/**
 * @param    string  $viewObjet          View object mostly send $this
 * @param    string  $viewFilePath       Path of view file to be rendered
 *
 *
 * @return    view                       Render View
 */

use optima\models\Cms;

$page_data = Cms::renderPage($viewObjet,$viewFilePath="404");

```
## Get Slugs

> * get array of all slugs

Example Usage : 
```php
/**
 * @param    string  $name          Name is type for getting slugs e.g "page"
 *
 *
 * @return    array                 User Data
 */

use optima\models\Cms;

$cms_model = Cms::Slugs($name)

```
Example Output:

```phparray
Array
(
    [0] => Array
        (
            [type] => page
            [slug] => home
            [slug_all] => Array
                (
                    [EN] => home
                    [ES] => home
                    [NL] => home
                    [DE] => home
                )

        )

)
```
## Cache Image

> * get URL of Cached Image

```php
/**
 * @param    string  $url          URL of the Image
 * @param    string  $name         Name of the Image
 * @param    string  $size         Size of Image
 *
 *
 * @return   string                URL
 */

use optima\models\Cms;

$img = Cms::CacheImage($url, $name, $size = 1200);
Example Usage : 
```
Example Output:

>"/uploads/temp/1200_Img"

## Cache Logo Icon

> * get URL of Cached Logo

Example Usage : 
```php
/**
 * @param    string  $name         Name of the Image
 *
 *
 * @return   string                URL
 */

use optima\models\Cms;

$logo = Cms::iconLogo($name);

```
Example Output:

>"https://images.optima-crm.com/uploads/cms_settings/5da80e18b15da74656087ca5/logo12345"

## Posts by Type (postTypes)

> * get array of posts from post type

Example Usage : 
```php
/**
 * @param    string   $name        name/key of post type
 * @param    string   $category    category of post type
 * @param    string   $forRoutes   route of post type
 * @param    integer  $pageSize    No of posts on a page
 *
 *
 * @return   array                 Data
 */

use optima\models\Cms;

$post = Cms::postTypes($name, $category = null, $forRoutes = null, $pageSize = 10);

```
Example Output:

```phparray
Array
(
    [0] => Array
        (
            [featured_image] => https://images.optima-crm.com/resize/cms_medias/112/1200/20191029083234000000_blog-5.jpg
            [content] => 
Personal guidance by an experienced real estate agency in Ibiza  
Perhaps you already know Ibiza Estates, because you once rented a holiday home in Ibiza with us. In addition to holiday rentals, we also focus on purchasing guidance. Ibiza Estates is also the right partner when it comes to sales support. Once you have taken the step of making your dream come true, we will make sure that at every next step, you will receive the right guidance that is fully adapted to your personal wishes.  

Ibiza Estates offers confidence when buying a holiday home in Ibiza  
Buying a house in the Netherlands is often a long and difficult process. Not to mention when it comes to a holiday home in Ibiza. You are probably unfamiliar with the Spanish laws and regulations and the language. All this can raise many questions that can lead to uncertainty, because you do not have all the facts. Ibiza Estates offers trust by mediating between you as the buying and selling party. With both offices in Eindhoven and Ibiza, we have a team of local and international experts, where we act as a neutral party.  

Holiday home Ibiza? We scan the entire market  
On our completely renewed website, you will find a clear selection of houses for sale in Ibiza. These are properties that we have exclusively in our portfolio. You can easily search on different regions and of course the budget. Is the holiday home in Ibiza of your dreams not included? Please contact us. Based on your search criteria, we will scan the entire market and contact our partners if necessary. In this way, you can see the entire market. Would you like to know more about our unique working method? Then you can read the step-by-step plan for purchasing support here.  

Ibiza Estates; experienced real estate agency in Ibiza  
The Ibiza Estates team is always there for you. We can visit you or you can come to one of our offices in Eindhoven or Ibiza. Our specialists are there to map out your wishes and realise your plans. This can be done in your own language, with Ibiza Estates acting as a mediator and interpreter. We have more than fifteen years of experience in real estate and we know the island inside out. Ibiza Estates is not only an expert in the field of legislation and regulations but is also aware of what is going on in all regions, so that we can provide you with appropriate advice. Where necessary, we make use of our team of lawyers and jurists. We also open our extensive network for you, because once you have entered your holiday home in Ibiza, our care does not stop. From the furnishing of your residence, good staff to a security system. Ibiza Estates is a one-stop-shop when it comes to realising and living your dream.  




            [created_at] => 2019-11-22T19:26:16+01:00
            [title] => Holiday home in Ibiza
            [slug] => een-vakantiehuis-op-ibiza-van-droom-tot-werkelijkheid
            [slug_all] => Array
                (
                    [EN] => een-vakantiehuis-op-ibiza-van-droom-tot-werkelijkheid
                    [NL] => een-vakantiehuis-op-ibiza-van-droom-tot-werkelijkheid
                )

            [meta_title] => Ibiza holiday home
            [meta_desc] => Of course, it’s nice to dream about something. Although it is even better to just do it. A holiday home in Ibiza does not have to be just a dream.
            [meta_keywords] => holiday home real estate experience
            [custom_settings] => Array
                (
                    [NL] => Array
                        (
                            [0] => Array
                                (
                                    [key] => publish-date
                                    [value] => 25-11-2019
                                )

                            [1] => Array
                                (
                                    [key] => title-detail
                                    [value] => Natuurlijk is het prettig om ergens over te dromen en te filosoferen. Al is het nog fijner om het gewoon te doen. Een vakantiehuis op Ibiza hoeft geen droom te blijven. Jij beschikt namelijk over de kracht om hier werkelijkheid van te maken. Waarbij je niet meteen de hele trap hoeft te bewandelen. Begin bij de eerste stap door contact met ons op te nemen. Ibiza Estates begeleidt u tijdens het gehele proces, zodat uw droom zo snel mogelijk tastbaar gemaakt wordt én u over het vakantiehuis van uw dromen beschikt.
                                )

                        )

                    [EN] => Array
                        (
                            [0] => Array
                                (
                                    [key] => publish-date
                                    [value] => 25-11-2019
                                )

                            [1] => Array
                                (
                                    [key] => title-detail
                                    [value] => Of course, it’s nice to dream and fantasise about something. Although it is even better to turn it into reality. A holiday home does not have to be just a dream; you can make this dream come true. And you don’t have to do it all by yourself. Start with the first step by contacting us. Ibiza Estates will guide you through the entire process, so that your dream comes true as soon as possible.
                                )

                        )

                )

            [categories] => Array
                (
                )

        )

    [1] => Array
        (
            [featured_image] => https://images.optima-crm.com/resize/cms_medias/112/1200/20191122193905000000_ibiza-island-boy-man-sea-travel-1422161-pxhere.jpg
            [content] => 
Watch the sunset at Es Vedrà  
There’s something about Ibiza. Whether it’s because of the film Fall in love with Ibiza or not, people from all over the world are attracted to this island. It is possible that the rock island Es Vedrà has something to do with this. When you wonder what are the highlights in Ibiza? Then you shouldn’t miss this sight. There are many myths and legends about Es Vedrà, but the fact is that it is one of the most magnetic places on earth. Only the North Pole and Bermuda triangle win from this rocky island. One could say that Es Vedrà works like a magnet. Once you’ve set foot on Ibiza, you keep coming back, don’t you? Watch the sunset from the viewpoint and see for yourself what this little island off the coast does to you. Who knows, you might spot a mermaid or a UFO. Do these observations belong to facts or myths? That’s up to you to decide.  

Visit one of the caves of Ibiza  
Of course, it’s wonderful to sit on your luxurious sunbed, or to visit one of Ibiza’s famous clubs. But the island has so much more to offer, also in terms of culture. In the north of Ibiza near Puerto de San Miguel, you will find the Cueva De Can Marca. Put this one on your list of Ibiza sights/what to do on Ibiza. When you enter this cave, you literally jump through time. You go back 100,000 years, when the cave was mainly used by smugglers. In addition, this is a useful sight for what to do in Ibiza when it rains, or what to do in Ibiza when it’s very hot.  

Spotting flamingos in Salinas  
Spotting flamingos? In Ibiza? Yes, you read it well. You don’t have to go all the way to Aruba to spot these graceful birds. In the south of Ibiza lies the Ses Salinas nature reserve, which is on the UNESCO World Heritage List. Here you will find the salt plains where you can walk endlessly and, with a bit of luck, see the flamingos bathe. There are also several beaches that are more than worthwhile, such as Es Cavallet where you can enjoy a delicious lunch at La Escollera. Or the beach of Salinas where Beso Beach is an excellent choice to spend a day.  All highlights in Ibiza.

Stroll through the charismatic Dalt Villa  
What to do in Ibiza? One of the most famous sights of Ibiza, a visit to Dalt Villa, cannot be missed. Dalt Villa is the old city centre of Ibiza Town, which is written in Catalan as Eivissa. When you walk through the impressive city walls, you will end up in the medieval old town. Every year, several events are organised here, such as the Ibiza Medieval Fair and Solomun also runs here once a year between the old city walls. The idyllic area is also a UNESCO World Heritage Site. Stroll through the romantic streets and eat at La Olivia. Walk straight on to the highest point for panoramic views over the harbour, where you can see the lights of club Lío shining over the water in the evening.  

Dance, shop or eat at Las Dalias  
The last on the list of What to do in Ibiza, these sights should not be missed is Las Dalias. Personally, we are not such a fan of the tourist hippy markets, but Las Dalias in San Carlos is of a different calibre. Here you can stroll around the authentic market all year round. From art, to leather goods and jewellery. Most of the items you’ll find here are made locally. Every Wednesday in high season, Namasté is organised and that is (again) a party of a very different kind. Here all free spirits come together to dance to Balearic Beats with the most beautiful light shows. Hippie, hipster or Quote-500 rating, everyone comes together here. Besides Las Dalias, Las Dalias Café is also one of the attractions of Ibiza that you want to try. Here you will find a varied menu that is suitable for both carnivores and herbivores and you can taste the authentic Ibiza.  

Cala Benirràs 
This beautiful beach in the north is usually an oasis of peace. Except on Sundays, when all the drummers of Ibiza gather here to celebrate life. On Sundays it is especially busy in the summer months, but that makes this place very vibrant. Do you want the golden tip what to do on Ibiza? Then book a table at beach restaurant Elements on Sunday. Also here on Sunday in the evening, the tables are put aside, and a DJ is playing great beats, creating the perfect ambiance. That is: a mix of the authentic hippie culture and the mundane Ibiza. Write this tip quickly on your list of highlights in Ibiza, because you don’t want to miss these sights either.  

https://www.elements-ibiza.com/ 


            [created_at] => 2019-11-21T19:57:10+01:00
            [title] => Highlights in Ibiza
            [slug] => wat-te-doen-op-ibiza-deze-bezienswaardigheden-mag-je-niet-missen
            [slug_all] => Array
                (
                    [EN] => wat-te-doen-op-ibiza-deze-bezienswaardigheden-mag-je-niet-missen
                    [NL] => wat-te-doen-op-ibiza-deze-bezienswaardigheden-mag-je-niet-missen
                )

            [meta_title] => What to do in Ibiza
            [meta_desc] => What do all Ibiza lovers have in common? They want new tips every time. Want to know what to do in Ibiza? These sights are not to be missed.
            [meta_keywords] => Dalt Villa Las Dallas Cala Benirras elements Salinas caves
            [custom_settings] => Array
                (
                    [0] => Array
                        (
                            [key] => title-detail
                            [value] => What do all Ibiza loving people have in common? They are always looking for new tips. No matter how often you go to Ibiza, there is always something to do. With more than 210 kilometres of beach, there are more than enough bays to discover. Besides the permanent sights, there are also the new hotspots that you want to admire. Ibiza Estates lists them, so that you always have your list of tips at hand.
                        )

                    [NL] => Array
                        (
                            [0] => Array
                                (
                                    [key] => publish-date
                                    [value] => 11-11-2019
                                )

                            [1] => Array
                                (
                                    [key] => title-detail
                                    [value] => Wat hebben alle Ibiza liefhebbende mensen met elkaar gemeen? Ze zijn telkens weer op zoek naar nieuwe tips. Hoe vaak je ook gaat er is altijd wat te doen op Ibiza. Met meer dan 210 kilometer aan strand, zijn er meer dan genoeg baaien om te ontdekken. Naast de blijvende bezienswaardigheden zijn het ook de nieuwe hotspots die je wilt bewonderen. Ibiza Estates zet ze vast op een rij, zodat je jouw lijst met tips altijd paraat hebt.
                                )

                        )

                    [EN] => Array
                        (
                            [0] => Array
                                (
                                    [key] => publish-date
                                    [value] => 11-11-2019
                                )

                            [1] => Array
                                (
                                    [key] => title-detail
                                    [value] => What do all Ibiza loving people have in common? They are always looking for new tips. No matter how often you go to Ibiza, there is always something to do. With more than 210 kilometres of beach, there are more than enough bays to discover. Besides the permanent sights, there are also the new hotspots that you want to admire. Ibiza Estates lists them, so that you always have your list of tips at hand.
                                )

                        )

                )

            [categories] => Array
                (
                )

        )

)
```
