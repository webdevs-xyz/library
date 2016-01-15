# Craft Snippets for PHPStorm

### Twig Tags (via tab trigger)

    }}              {{  }}
    %%              {%  %}
    ##              {#  #}

    extends         {% extends 'template' %}
    inc             {% include 'template' with vars %}
    incp            {% include 'template' with {
                      key: 'value'
                    }} %}

    set, setb       {% set var = value %}
    block, blockb   {% block name %} ... {% endblock %}
    filter, filterb {% filter name %} ... {% endfilter %}

    if, ifb         {% if condition %} ... {% endif %}
    ife             {% if condition %} ... {% else %} ... {% endif %}
    for             {% for item in seq %} ... {% endfor %}
    fore            {% for item in seq %} ... {% else %} ... {% endfor %}
    else            {% else %}

    endif           {% endif %}
    endfor          {% endfor %}
    endset          {% endset %}
    endblock        {% endblock %}
    endfilter       {% endfilter %}

### Twig Tags, Customized for Craft (via tab trigger)

    assets, assetsp          craft.assets loop
    categories, categoriesp  craft.categories loop
    entries, entriesp        craft.entries loop
    feed                     craft.feeds.getFeedItems loop
    tags, tagsp              craft.tags loop
    users, usersp            craft.users loop

    ciel               ceil()
    csrf               {{ getCsrfInput() }}
    exit               {% exit 404 %}
    floor              floor()
    includecss         {% includeCssFile "/resources/css/global.css" %}
    includejs          {% includeJsFile "/resources/css/global.css" %}
    matrix             Outputs a basic Matrix Field loop
    max                max()
    min                min()
    paginate           Simple:   Outputs an example of pagination with craft.entries
    paginateb          Advanced: Outputs an example of pagination with craft.entries
    redirect           {% redirect 'login' %}
    requestParam       craft.request.getParam()
    requestPost        craft.request.getPost()
    requestQuery       craft.request.getQuery()
    requestSegment     craft.request.getSegment()
    requirelogin       {% requireLogin %}
    requirepermission  {% requirePermission "spendTheNight" %}
    round              round()
    shuffle            shuffle()
    switch             {% switch variable %}{% endswitch %}
    url, urla          url('path'), url('path', params, 'http', false)