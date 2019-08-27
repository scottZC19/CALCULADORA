# CALCULADORA
calculadora realizado en java
//para las operaciones 
package calculadora;


public class Operaciones {
    // atributos
    protected double nro1;
    protected double nro2;
    // propiedades
    public double getNro1()
    {
        return this.nro1;
    }
    public double getNro2()
    {
        return this.nro2;
    }
    public void setNro1 (double nro1)
    {
        this.nro1 = nro1;
    }
    public void setNro2 (double nro2)
    {
        this.nro2 = nro2;
    }
    
    //Constructrores
    //1-constructores sin sobrecarga de parametros
    public Operaciones ()
    {}
    //2-constructores con sobrecarga de parametros
    public Operaciones(double nro1, double nro2)
    {
        this.nro1 = nro1;
        this.nro2 = nro2;
    }
    //Implementacion de metodos u operaciones
    public double Sumar()
    {
        return this.nro1 + this.nro2;
    }
    public double Restar()
    {
        return this.nro1 - this.nro2;
    }
    public double Multiplicar()
    {
        return this.nro1 * this.nro2;
    }
    public String Dividir()
    {
        if(this.nro2 == 0)
        {  
            return "Error: Indeterminado";
        }
        else
        {
            double dividir = this.nro1/this.nro2;
            return String.valueOf(dividir);
        }
                
    }
    public double Potencia()
    {
        double Pot = 1;
        for (int i = 1; i<=this.nro2; i++){
            Pot *= this.nro1;
        }
        return Pot;
    }
    private double Fac(double nro)
    {
        if (nro==0){
            return 1;
        }
        else
            return nro * Fac(nro-1);
    }
    public double Factorial()
    {
        return Fac(this.nro1);
    }
    public double Raiz()
    {
        return Math.sqrt(this.nro1);
    }
    public double Seno()
    {
        return Math.sin(Math.toRadians(this.nro1));
    }
    public double Coseno()
    {
        return Math.sin(Math.toRadians(this.nro1));
    }
    public double Tangente()
    {
        return Math.sin(Math.toRadians(this.nro1));
    }
}
