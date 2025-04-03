# Teste de Datas Git

Data completa: {{ git_revision_date_localized }}

Data ISO: {% if git_revision_date_localized_iso %}{{ git_revision_date_localized_iso }}{% else %}Não disponível{% endif %}

Tempo relativo: {% if git_revision_date_localized_timeago %}{{ git_revision_date_localized_timeago }}{% else %}Não disponível{% endif %}