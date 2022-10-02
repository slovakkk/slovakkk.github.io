# slovakkk.github.io
                        if (data != null) {
                            var StringValue = data
                            var ArrayValues = StringValue.split(",");
                            $('#thermometer').html('<em class="ion-thermometer"></em> Temperatura actual: ' + ArrayValues[0]);
                            $('#climamo').html(ArrayValues[0]);
                            $("#weather").attr("src", ArrayValues[1]);
                        }
                    }
                });
            }

            // obtiene el clima del fondo
            function climaFondo() {
                $.ajax({
                    cache: false,
                    //                    url: '/climafeed/?ci=' + $("#lat_position").val(),
                    url: '/pronosticoclima/mochis',
                    success: function (data) {
                        if (data != null) {
                            $('#clima').html(data);
                            $(".weather-fbx").fancybox({
                                maxWidth: 956,
                                maxHeight: 501,
                                fitToView: false,
                                width: '100%',
                                height: '90%',
                                autoSize: false,
                                closeClick: false,
                                openEffect: 'none',
                                closeEffect: 'none',
                                padding: 0,
                                helpers: {
                                    overlay: {
                                        css: {
                                            'background': 'rgba(51, 51, 51, 0.6)'
                                        }
                                    }
                                },
                                afterLoad: function () {
                                    setTimeout(function () {
                                        $(".next-week").slick({
                                            infinite: true,
                                            lazyLoad: 'progressive',
                                            slidesToShow: 4,
                                            slidesToScroll: 1,
                                            responsive: [
                                                {
                                                    breakpoint: 1024,
                                                    settings: {
                                                        slidesToShow: 3,
                                                        slidesToScroll: 1
                                                    }
                                                }
                                            ]
                                        });
                                        $(".next-week").on('init', function (event, slick, currentSlide, nextSlide) {
                                            $(".next-week")[0].slick.setPosition();
                                        });
                                    }, 4000);
                                }
                            });
                        }

                        ChangeValue("Clima actual");
                    }
                });
            }


            function getWeather() {
                var cityId = $("#slcClima").val();
                if (cityId == null || cityId == "") {
                    alert("Favor de ingresar tu ubicaci&oacute;n.");
                }
                else {
                    $.ajax({
                        cache: false,
                        url: '/climafeed/?ci=' + cityId,
                        success: function (data) {
                            if (data != null) {
                                $('#clima').html(data);
                                $(".weather-fbx").fancybox({
                                    maxWidth: 956,
                                    maxHeight: 501,
                                    fitToView: false,
                                    width: '100%',
                                    height: '90%',
                                    autoSize: false,
                                    closeClick: false,
                                    openEffect: 'none',
                                    closeEffect: 'none',
                                    padding: 0,
                                    helpers: {
                                        overlay: {
                                            css: {
                                                'background': 'rgba(51, 51, 51, 0.6)'
                                            }
                                        }
                                    },
                                    afterLoad: function () {
                                        setTimeout(function () {
                                            $(".next-week").slick({
                                                infinite: true,
                                                lazyLoad: 'progressive',
                                                slidesToShow: 4,
                                                slidesToScroll: 1,
                                                responsive: [
                                                    {
                                                        breakpoint: 1024,
                                                        settings: {
                                                            slidesToShow: 3,
                                                            slidesToScroll: 1
                                                        }
                                                    }
                                                ]
                                            });
                                            $(".next-week").on('init', function (event, slick, currentSlide, nextSlide) {
                                                $(".next-week")[0].slick.setPosition();
                                            });
                                        }, 100);
                                    }
                                });
                                ChangeValue(cityId);
                            }
                            setTimeout(function () {
                                $(".next-week").slick({
                                    infinite: true,
                                    lazyLoad: 'progressive',
                                    slidesToShow: 4,
                                    slidesToScroll: 1,
                                    responsive: [
                                        {
                                            breakpoint: 1024,
                                            settings: {
                                                slidesToShow: 3,
                                                slidesToScroll: 1
                                            }
                                        }
                                    ]
                                });
                                $(".next-week").on('init', function (event, slick, currentSlide, nextSlide) {
                                    $(".next-week")[0].slick.setPosition();

                                });
                            }, 100);
                        }
                    });
                }

            }

            function popitup(url) {
                newwindow = window.open(url, 'stereo1', 'height=600,width=600');
                if (window.focus) { newwindow.focus() }
                return false;
            }

            function ChangeValue(ubicacion) {
                $(".weather-title #title_weather").text(ubicacion);
                $("#title_weather").css("text-transform", "uppercase");
            }
        </script><script>
                                var meses = new Array("enero", "febrero", "marzo", "abril", "mayo", "junio", "julio", "agosto", "septiembre", "octubre", "noviembre", "diciembre");
                                var dia = new Array("Domingo", "Lunes", "Martes", "Mi&eacute;rcoles", "Jueves", "Viernes", "S&aacute;bado", "Domingo");
                                var f = new Date();
                                $('#hdate').html(dia[f.getDay()] + " " + f.getDate() + " de " + meses[f.getMonth()] + " de " + f.getFullYear());

                                function mostrarmodalradios() {
                                    $("#modalradios").css("display", "block");
                                    $("#masthead").css("display", "none");
                                }

                                function ocultarmodalradios() {
                                    $("#modalradios").css("display", "none");
                                    $("#masthead").css("display", "block");
                                }

                            </script><script>
                    $(document).ready(function () {

                        

                        _gaq.push(["_trackEvent", "NOTA-EDITOR", "carlosvega81@gmail.com", "/2022-10-01/seguridad/por-robo-en-tiendas-de-guamuchil-lo-vinculan-a-proceso/148371", , false]);

                                               

                    });
                </script><script type="text/javascript">
                            $.ajax({
                                cache: false,
                                url: '/lasmasleidasdia/',
                                success: function (data)
                                {
                                    //if (data.length < 200) {
                                    $('#lasmasleidas').append(data);
                                    //}
                                }
                            });
                        </script><script type="text/javascript">
                            $(document).ready(function () {
                                var strUrlPost = 'https://www.luznoticias.mx/xstatic/luznoticias/template/submitaddclickstory.aspx?id=148371';
                                $.post(strUrlPost, function (data) {
                                    var valretorno;
                                    valretorno = data;
                                });
                            });
                        </script><script>
    if ('serviceWorker' in navigator) {
        window.addEventListener('load', function () {
            navigator.serviceWorker.register('https://www.luznoticias.mx/sw').then(function (registration) {
                console.log('ServiceWorker registration successful with scope: ', registration.scope);
            }, function (err) {
                console.log('ServiceWorker registration failed: ', err);
            });
        });
    }
</script><iframe src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/container(2).html" style="visibility: hidden; display: none;"></iframe>
<div id="onesignal-bell-container" class="onesignal-bell-container onesignal-reset onesignal-bell-container-bottom-right"><div id="onesignal-bell-launcher" class="onesignal-bell-launcher onesignal-bell-launcher-md onesignal-bell-launcher-bottom-right onesignal-bell-launcher-theme-default onesignal-bell-launcher-active" style="bottom: 15px; right: 15px;"><div class="onesignal-bell-launcher-button"><svg class="onesignal-bell-svg" xmlns="http://www.w3.org/2000/svg" width="99.7" height="99.7" viewBox="0 0 99.7 99.7" style="filter: drop-shadow(0 2px 4px rgba(34,36,38,0.35));; -webkit-filter: drop-shadow(0 2px 4px rgba(34,36,38,0.35));;"><circle class="background" cx="49.9" cy="49.9" r="49.9" style="fill: rgb(39, 23, 154);"></circle><path class="foreground" d="M50.1 66.2H27.7s-2-.2-2-2.1c0-1.9 1.7-2 1.7-2s6.7-3.2 6.7-5.5S33 52.7 33 43.3s6-16.6 13.2-16.6c0 0 1-2.4 3.9-2.4 2.8 0 3.8 2.4 3.8 2.4 7.2 0 13.2 7.2 13.2 16.6s-1 11-1 13.3c0 2.3 6.7 5.5 6.7 5.5s1.7.1 1.7 2c0 1.8-2.1 2.1-2.1 2.1H50.1zm-7.2 2.3h14.5s-1 6.3-7.2 6.3-7.3-6.3-7.3-6.3z" style="fill: rgb(255, 255, 255);"></path><ellipse class="stroke" cx="49.9" cy="49.9" rx="37.4" ry="36.9" style="stroke: rgb(255, 255, 255);"></ellipse></svg></div><div class="onesignal-bell-launcher-badge" style="filter: drop-shadow(0 2px 4px rgba(34,36,38,0));; -webkit-filter: drop-shadow(0 2px 4px rgba(34,36,38,0));;"></div><div class="onesignal-bell-launcher-message"><div class="onesignal-bell-launcher-message-body">Suscríbete a nuestras notificaciones</div></div><div class="onesignal-bell-launcher-dialog" style="filter: drop-shadow(0px 2px 2px rgba(34,36,38,.15));; -webkit-filter: drop-shadow(0px 2px 2px rgba(34,36,38,.15));;"><div class="onesignal-bell-launcher-dialog-body"></div></div></div></div><iframe width="0" height="0" frameborder="none" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/saved_resource(4).html"></iframe><iframe height="0" width="0" frameborder="0" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/tag.html" style="display: none;"></iframe><iframe src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/html.html" width="1" height="1" style="display: none;"></iframe><div class="hybs-slot" id="hybs-slot-8346" style="margin: 0px auto; position: absolute; max-width: 600px; left: 228.25px; opacity: 1; transition: opacity 1s ease 0s; height: 600px; width: 600px; top: 1277.09px; text-align: center;"><iframe scrolling="no" frameborder="0" id="hybs-dp-iframe-8346" style="position: absolute; display: flex; height: 600px;" height="600" width="100%" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/saved_resource(5).html"></iframe></div><iframe id="rdr_1609_6436" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/Aw0CBBAUGCgqNHbCAcwBhAKwBA.html" style="height: 1px; width: 1px; border: none; position: absolute; top: -100px; left: -100px; z-index: -5;"></iframe><iframe src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/aframe.html" width="0" height="0" style="display: none;"></iframe></body><iframe id="google_esf" name="google_esf" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/zrt_lookup.html" style="display: none;"></iframe><iframe sandbox="allow-scripts allow-same-origin" id="38c39c20e6b01c" frameborder="0" allowtransparency="true" marginheight="0" marginwidth="0" width="0" hspace="0" vspace="0" height="0" style="height:0px;width:0px;display:none;" scrolling="no" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/sync.html">
    </iframe><iframe sandbox="allow-scripts allow-same-origin" id="39e4388b7493645" frameborder="0" allowtransparency="true" marginheight="0" marginwidth="0" width="0" hspace="0" vspace="0" height="0" style="height:0px;width:0px;display:none;" scrolling="no" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/async_usersync.html">
    </iframe><iframe sandbox="allow-scripts allow-same-origin" id="4095378b6526663" frameborder="0" allowtransparency="true" marginheight="0" marginwidth="0" width="0" hspace="0" vspace="0" height="0" style="height:0px;width:0px;display:none;" scrolling="no" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/beacon.html">
    </iframe><iframe sandbox="allow-scripts allow-same-origin" id="41688aa4330b39" frameborder="0" allowtransparency="true" marginheight="0" marginwidth="0" width="0" hspace="0" vspace="0" height="0" style="height:0px;width:0px;display:none;" scrolling="no" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/pd.html">
    </iframe><iframe sandbox="allow-scripts allow-same-origin" id="42ed25ce21313f6" frameborder="0" allowtransparency="true" marginheight="0" marginwidth="0" width="0" hspace="0" vspace="0" height="0" style="height:0px;width:0px;display:none;" scrolling="no" src="./Por robo en tiendas de Guamúchil, lo vinculan a proceso_files/iframe.html">
    </iframe></html>[1.txt](https://github.com/slovakkk/slovakkk.github.io/files/9692722/1.txt)
[1(1).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692723/1.1.txt)
[1.txt](https://github.com/slovakkk/slovakkk.github.io/files/9692724/1.txt)
![5a5b4803e9e841d7bd58ba7a7afb05dd_131989f08a7766537667c643f71683a9](https://user-images.githubusercontent.com/68411624/193457990-c1ca426a-0e84-4b34-84ed-7b268b3d06df.png)
![22e553a9689a4aca958d035b1eb147ae_5a0dcb9f1f54c4d8ffe2fdcdc1be0065](https://user-images.githubusercontent.com/68411624/193457993-320de8b4-e981-4ad2-a879-f52ecdd5890b.png)
![355_791logo](https://user-images.githubusercontent.com/68411624/193457994-63d98288-a40a-4e08-9317-1663ba17acf2.png)
![7529e2c1ff0c49f8a81dd8391e31787e_ce051e792eaeaad8dd38c13ec10bac45](https://user-images.githubusercontent.com/68411624/193457995-99c3ed0d-060c-46c7-8eb7-37e52a1c1478.png)
![711169](https://user-images.githubusercontent.com/68411624/193457997-e9a5abce-65d7-4e7e-a5cb-abfa6c44cab6.gif)
![App Menu-13](https://user-images.githubusercontent.com/68411624/193457998-8fb8cfbe-5f14-468d-91e7-082b60e26dd2.jpg)
![back_button2](https://user-images.githubusercontent.com/68411624/193457999-329bb20a-e3dc-493d-a7f0-2d82706db3a5.svg)
![clima-despejado-icon1](https://user-images.githubusercontent.com/68411624/193458000-c0f22fa8-1ab5-4049-94e9-d8bb633e9f66.png)
![close_button_gray](https://user-images.githubusercontent.com/68411624/193458001-7bce47e8-0235-45b9-bf01-cc394caf018f.svg)
![criteo_logo_2021](https://user-images.githubusercontent.com/68411624/193458003-7d4f5ca1-3da5-4293-9991-2375f8b3eaef.svg)
![es](https://user-images.githubusercontent.com/68411624/193458004-46bb0d58-c949-473e-b946-68da11f698ae.png)
[f(1).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692725/f.1.txt)
[f(2).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692726/f.2.txt)
[f(3).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692727/f.3.txt)
[f(4).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692728/f.4.txt)
[f(5).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692729/f.5.txt)
[f(6).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692731/f.6.txt)
[f(7).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692732/f.7.txt)
[f(8).txt](https://github.com/slovakkk/slovakkk.github.io/files/9692733/f.8.txt)
[f.txt](https://github.com/slovakkk/slovakkk.github.io/files/9692734/f.txt)
![GzgedhmzSQa](https://user-images.githubusercontent.com/68411624/193458009-e10bbb86-e368-4e2a-beb2-bf19f5f7d0da.png)
![hddesktop-2626x1067-neo-2fa44a72](https://user-images.githubusercontent.com/68411624/193458012-3edb3d06-da04-422b-9f42-4e49ebf0be06.png)
![hddesktop-2626x1067-siempre-b736311b](https://user-images.githubusercontent.com/68411624/193458013-90e78b1d-478a-41fb-b361-6f52adb6c6de.png)
![i_big_tr](https://user-images.githubusercontent.com/68411624/193458014-c26e3962-bae3-4c04-8ccc-752c3f5b46be.svg)
![i_small_tr](https://user-images.githubusercontent.com/68411624/193458015-d7439c2a-a5bb-4c04-a55c-f978437ccf37.svg)
![icon](https://user-images.githubusercontent.com/68411624/193458016-be9a435c-71b4-41b8-a519-9508e0be7693.png)
![ln](https://user-images.githubusercontent.com/68411624/193458017-16743a58-1494-4022-9ccb-7d5d5b16c1d2.png)
![luz_logo](https://user-images.githubusercontent.com/68411624/193458018-eb75ce6a-3256-402c-a513-49c5461df33e.png)
![neoculiacan](https://user-images.githubusercontent.com/68411624/193458019-34be0507-45c6-43e2-9c86-29b47623e144.jpg)
![privacy](https://user-images.githubusercontent.com/68411624/193458021-020be560-87c2-4541-8a4d-a2e8a4264b1e.svg)
![radioenvivo_blanco](https://user-images.githubusercontent.com/68411624/193458023-d46b76ba-8750-45da-9101-a004cbae01b4.png)
![radioslateral](https://user-images.githubusercontent.com/68411624/193458025-550d1283-676b-4bee-8dd0-670196628928.png)
![seguridad2](https://user-images.githubusercontent.com/68411624/193458026-491d746b-115c-4071-bd9b-798064a28bb0.jpg)
![siempreculiacan](https://user-images.githubusercontent.com/68411624/193458027-71957d16-16b5-406f-a44b-60e60a969a41.jpg)
![stereo1culiacan](https://user-images.githubusercontent.com/68411624/193458028-8431de3a-db47-4afa-a756-1f64ed9f7369.jpg)
![stereo1losmochis](https://user-images.githubusercontent.com/68411624/193458030-6366fe00-0d40-4761-b4b6-af2d10eccbfa.png)
![tvenvivo_blanco](https://user-images.githubusercontent.com/68411624/193458031-332f926e-b553-44e2-81a0-25c35c7781cb.png)
![vintage](https://user-images.githubusercontent.com/68411624/193458032-b631cf41-ad05-4dcc-b4dc-b4da6e3dd6f0.png)
![vintagecln](https://user-images.githubusercontent.com/68411624/193458033-c8af67da-2ae5-4c1f-ad90-17ef5e350379.jpg)
![webdesktop-2626x1067-la-morrita-d6b57c68](https://user-images.githubusercontent.com/68411624/193458035-30ae786f-96c4-44ea-ab64-28e2aef4a905.jpg)
![whatsappimage20210414at2 02 54pm-focus-0-0-698-429](https://user-images.githubusercontent.com/68411624/193458036-9694d552-6c21-4142-a9c7-19c8a66adaa2.jpg)
