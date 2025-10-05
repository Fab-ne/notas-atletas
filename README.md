class Funcionario {
    constructor(nome, sobrenome, cargo) {
        this.nome = nome;
        this.sobrenome = sobrenome;
        this.cargo = cargo;
    }

    obterNomeCompleto() {
        return `${this.nome} ${this.sobrenome}`;
    }

    obterIniciais() {
        return this.nome[0] + this.sobrenome[0];
    }

    obterPosicao() {
        return `${this.nome} trabalha como ${this.cargo}`;
    }
}

class Gerente extends Funcionario {
    obterNomeCompleto() {
        return `${this.nome} ${this.sobrenome} [gerente]`;
    }

    obterPosicao() {
        return `${this.nome} é o gerente`;
    }
}

let sueli = new Funcionario("Sueli", "Borges", "desenvolvedora");
console.log(sueli.obterNomeCompleto()); 
console.log(sueli.obterIniciais());     
console.log(sueli.obterPosicao());      

let carlos = new Gerente("Carlos", "Santos", "gerente");
console.log(carlos.obterNomeCompleto()); 
console.log(carlos.obterIniciais());     
console.log(carlos.obterPosicao());      
