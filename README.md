<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Supabase Demo</title>
  <link rel="stylesheet" href="supa.css">
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
</head>
<body>
  <script>
    const { createClient } = window.supabase;
    const SUPABASE_URL = 'https://jupohrshthzchxxwfsti.supabase.co';
    const SUPABASE_ANON_KEY = 'sb_publishable_Hn8VHrZSisY1OrPXOLLQew_p3PaNz1W';
    const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);
    async function loadData() {
      const { data, error } = await supabase.from('название_таблицы').select('*');
      if (error) console.error('Ошибка:', error);
      else console.log('Данные:', data);
    }
    loadData();
  </script>
</body>
</html>
