import React, { useState, useEffect } from 'react';

const Contador = () => {

    const [contador, setContador] = useState(0);

    
    useEffect(() => {
        console.log(`El contador cambió a: ${contador}`);

    }, [contador]); 


    const aumentar = () => setContador(contador + 1);
    const disminuir = () => setContador(contador - 1);

    return (
        <div className="contador text-center mt-5">
            <h1>🧮 Contador React</h1>
            <h2>{contador}</h2>
            <div className="d-flex justify-content-center gap-2">
                <button className="btn btn-success" onClick={aumentar}>➕ Aumentar</button>
                <button className="btn btn-danger" onClick={disminuir}>➖ Disminuir</button>
            </div>
        </div>
    );
}

export default Contador;
