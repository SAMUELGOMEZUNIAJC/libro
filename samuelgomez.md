public class Libro {
    protected String titulo;
    protected String autor;
    protected String propietario;
    protected double precio;
    
    public Libro(String titulo, String autor, String propietario, double precio) {
        this.titulo = titulo;
        this.autor = autor;
        this.propietario = propietario;
        this.precio = precio;
    }

    public String getTitulo() {
        return titulo;
    }

    public void setTitulo(String titulo) {
        this.titulo = titulo;
    }

    public String getAutor() {
        return autor;
    }

    public void setAutor(String autor) {
        this.autor = autor;
    }

    public String getPropietario() {
        return propietario;
    }

    public void setPropietario(String propietario) {
        this.propietario = propietario;
    }

    public double getPrecio() {
        return precio;
    }

    public void setPrecio(double precio) {
        this.precio = precio;
    }

    public void imprimir(){
        System.out.println("el titulo es: " + titulo );
        System.out.println(" el autor es: " + autor);
        System.out.println("el precio del libro es:  " + precio);
    }


}


------------------------------------------------------------------------------


public class LibroDeTexto extends Libro{
    private String curso;
    
  
    public LibrosDeTexto(String titulo, String autor, String propietario, double precio, String curso) {
        super(titulo, autor, propietario, precio);
        //TODO Auto-generated constructor stub
        this.curso = curso;
    }

    public String getCurso() {
        return curso;
    }
    
    
    public void setCurso(String curso) {
        this.curso = curso;
    }
    

    public void ImprimirAqui(){
        super.imprimir();
        System.out.println("el curso es: " + curso);
    }

}

-----------------------------------------------------------------------------------

public class LibroDeTextoInstitucion extends LibrosDeTexto {
    private String facultad;

    public LibroDeTextoInstitucion(String titulo, String autor, String propietario, double precio, String curso,String facultad) {
        super(titulo, autor, propietario, precio, curso);
        //TODO Auto-generated constructor stub
        this.facultad = facultad;
    }
    
    public void imprimirAqui(){
        super.imprimir();
        System.out.println("la facultad es: " + facultad);
    }
}

-----------------------------------------------------------------------------------

public class Novelas  extends LibroDeTextoInstitucion{
    private String tiposNovelas;

    public Novelas(String titulo, String autor, String propietario, double precio, String curso, String facultad, String tipoNovelas) {
        super(titulo, autor, propietario, precio, curso, facultad);
        //TODO Auto-generated constructor stub
        this.tiposNovelas = tipoNovelas;
    }


    public String getTiposNovelas() {
        return tiposNovelas;
    }

    public void setTiposNovelas(String tiposNovelas) {
        this.tiposNovelas = tiposNovelas;
    }

    public void imprimirAqui3(){
        super.imprimir();
        System.out.println(" el tipo de novela es: " + tiposNovelas);
    }

}

----------------------------------------------------------------------------------------------

public class main {
    public static void main(String[] args) {
        
        Libro libro1 = new Libro(titulo:null, Autor:null, propietario:null, precio:0);
        libro1.setTitulo(titulo:" Harold ");
        libro1.setAutor(autor:"Brayan hoconer ");
        libro1.setPropietario(propietario:" samuel");
        libro1.setPrecio(precio:45000);
        libro1.imprimir();

        LibrosDeTexto libro2 = new LibrosDeTexto(titulo:null, Autor:null, propietario:null, precio:0 curso:null);
        libro2.setTitulo(titulo:" la maldicion de sofia ");
        libro2.setAutor(autor:"richar atikles ");
        libro2.setPropietario(ropietario:" samuel");
        libro2.setCurso(curso:"B11")
        libro2.setPrecio(precio:35000);
        libro2.imprimirAqui1();

        LibrosDeTextoInstitucion libro3 = new LibroDeTextoInstitucion(titulo:null, Autor:null, propietario:null, precio:0 curso:null);
        libro3.setTitulo(titulo:" la zorra mortal ");
        libro3.setAutor(autor:"Lial nimson ");
        libro3.setPropietario(propietario:" samuel");
        libro3.setFcultad(facultad:"increible")
        libro3.setPrecio(precio:40000);
        libro3.imprimirAqui2();

        Novelas libro4 = new Novelas(titulo:null, autor:null, propietario:null, precio:0, tipoNovelas:null, null, null);
        libro4.setTitulo(titulo:" dragon ball ");
        libro4.setAutor(autor:" toyotaro ");
        libro4.setPropietario(propietario:" toriyama");
        libro4.setPrecio(precio:73000);
        libro4.setTiposNovelas(tipoNovelas:" anime");
        libro4.imprimirAqui3();
    }

}
