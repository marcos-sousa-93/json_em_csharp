## Criar arquivo JSON com C#
<ul><li>Criar classe ArquivoJson</li></ul>

<pre>
  <code>
public class ArquivoJson {

}
  </code>
</pre>

<ul><li>Criar método CriarArquivo que recebe um parâmetro do tipo string.</li></ul>

<pre>
  <code>
public void CriarArquivo(string arquivo) {

}
  </code>
</pre>

<ul><li>Defina o caminho e o nome do arquivo que você deseja criar</li></ul>

<pre>
  <code>
string caminhoArquivo = arquivo;
  </code>
</pre>

<ul><li>Verifique se o arquivo já existe</li></ul>

<pre>
  <code>
if (File.Exists(caminhoArquivo)) {
    // Verdadeiro se o arquivo existir.
} else {
    // Falso se o arquivo não existir.
    string conteudoJson = "";
    // Cria um novo arquivo no caminho especificado por "caminhoArquivo" e escreve o conteúdo de "conteudoJson" nele.
    File.WriteAllText(caminhoArquivo, conteudoJson);
    Console.WriteLine("Arquivo criado com sucesso.");
}
  </code>
</pre>

<ul><li>Código completo:</li></ul>

<pre>
  <code>
public class ArquivoJson {

    public void CriarArquivo(string arquivo) {
    
        string caminhoArquivo = arquivo;

        if (File.Exists(caminhoArquivo)) {
    
            Console.WriteLine("Um arquivo com esse nome já existe.");
            
        } else {
    
            string conteudoJson = "";
    
            if (conteudoJson == "") {
    
                File.WriteAllText(caminhoArquivo, conteudoJson);
    
                Console.WriteLine("Arquivo criado com sucesso.");
                
            }
        }
    }
}
  </code>
</pre>
