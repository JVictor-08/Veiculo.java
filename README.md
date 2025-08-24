public class Veiculo {
    String modelo;
    String cor;
    int ano;
    boolean ligado;

    public Veiculo(String modelo, String cor, int ano, boolean ligado) {
        this.modelo = modelo;
        this.cor = cor;
        this.ano = ano;
        this.ligado = ligado;
    }

    public void ligar() {
        if (!ligado) {
            ligado = true;
            System.out.println("O veículo foi ligado.");
        } else {
            System.out.println("O veículo já está ligado.");
        }
    }

    public void desligar() {
        if (ligado) {
            ligado = false;
            System.out.println("O veículo foi desligado.");
        } else {
            System.out.println("O veículo já está desligado.");
        }
    }

    public void acelerar() {
        if (ligado) {
            System.out.println("O veículo está acelerando!");
        } else {
            System.out.println("Você precisa ligar o veículo primeiro.");
        }
    }

    public static void main(String[] args) {
        Veiculo meuCarro = new Veiculo("Fusca", "Azul", 1975, false);

        System.out.println("Modelo: " + meuCarro.modelo);
        System.out.println("Cor: " + meuCarro.cor);
        System.out.println("Ano: " + meuCarro.ano);

        meuCarro.acelerar();  
        meuCarro.ligar();     
        meuCarro.acelerar();  
        meuCarro.desligar();  
    }
}s
