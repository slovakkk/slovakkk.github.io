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
    </iframe></html>
